# Balatero Elite - Vehicle Rental App

A modern vehicle rental application with admin dashboard.

## Features

- Vehicle listings with filtering
- Online booking system
- Admin dashboard with statistics
- Booking management (confirm, cancel, delete)
- Supabase integration for database and authentication
- LocalStorage fallback for demo purposes

## Setup Instructions

### 1. Supabase Setup

1. Create a new project on [Supabase](https://supabase.com)
2. Create a `bookings` table with the following columns:
   - `id` (uuid, primary key)
   - `vehicle_id` (int8)
   - `vehicle_name` (text)
   - `vehicle_type` (text)
   - `customer_name` (text)
   - `customer_email` (text)
   - `customer_phone` (text)
   - `pickup_date` (date)
   - `return_date` (date)
   - `days` (int8)
   - `total` (int8)
   - `status` (text, default: 'pending')
   - `created_at` (timestamptz, default: now())

3. Enable Row Level Security (RLS) and create policies
4. Create an admin user in Authentication > Users
5. Get your Project URL and Anon Key from Project Settings > API

### 2. Configure the App

Open `index.html` and replace:
- `YOUR_SUPABASE_URL` with your Supabase Project URL
- `YOUR_SUPABASE_ANON_KEY` with your Supabase Anon Key

### 3. Demo Login (without Supabase)

You can use the demo credentials without setting up Supabase:
- Email: `admin@demo.com`
- Password: `demo123`

### 4. GitHub Setup

1. Initialize git: `git init`
2. Add files: `git add .`
3. Commit: `git commit -m "Initial commit"`
4. Create a repository on GitHub
5. Push to GitHub: `git remote add origin <your-repo-url> && git push -u origin main`

### 5. Deploy to Vercel

1. Connect your GitHub repository to Vercel
2. Import the project
3. Deploy! Vercel will automatically deploy static sites

## Technologies Used

- HTML5
- CSS3
- Vanilla JavaScript
- Supabase (database, auth)
- Vercel (hosting)
- GitHub (version control)
