-- Run once in Supabase > SQL Editor
create table kv (key text primary key, value jsonb not null);
alter table kv enable row level security;
create policy "app access" on kv for all using (true) with check (true);
