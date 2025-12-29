# TallyCare - B2B Ticketing System

A Flutter-based support ticketing system for Tally Service Providers, built with Clean Architecture and Supabase.

## Current Status ✅

### Completed
- ✅ **Clean Architecture Structure**: Domain, Data, Presentation layers
- ✅ **Supabase Integration**: Connected to your Supabase instance
- ✅ **Data Models**: `Ticket` and `User` entities (Freezed)
- ✅ **Repository Pattern**: `SupabaseTicketRepository` for data operations
- ✅ **Agent Dashboard**: UI with analytics (Pie Chart for ticket stats)
- ✅ **Riverpod Providers**: State management setup
- ✅ **Build Runner**: Generated files successfully

### Database Setup Required
1. Run the SQL migration in Supabase Dashboard:
   - File: `supabase/migrations/20250524000000_initial_schema.sql`
2. Run the seed data:
   - File: `supabase/seed.sql`
   - Creates test users: `admin/admin123` and `agent/agent123`

## Running the App

```bash
# Install dependencies
flutter pub get

# Run on Windows
flutter run -d windows

# Run on Android
flutter run -d android
```

## Tech Stack
- **Framework**: Flutter (latest stable)
- **Backend**: Supabase (PostgreSQL, Realtime, Storage)
- **State Management**: Riverpod (with code generation)
- **Architecture**: Clean Architecture + MVVM
- **Navigation**: GoRouter
- **UI**: FlexColorScheme, Google Fonts, fl_chart

## Project Structure
```
lib/
├── core/
│   └── error/
│       └── failures.dart
├── features/
│   ├── auth/
│   │   ├── domain/entities/
│   │   └── presentation/pages/
│   ├── tickets/
│   │   ├── domain/
│   │   │   ├── entities/
│   │   │   └── repositories/
│   │   ├── data/repositories/
│   │   └── presentation/
│   │       ├── providers/
│   │       └── pages/
│   └── dashboard/
│       └── presentation/
│           ├── pages/
│           └── widgets/
└── main.dart
```

## Next Steps (Pending)
- [ ] Implement Login Page logic
- [ ] Add Ticket Detail Page
- [ ] Create Ticket Form
- [ ] Role-based routing (Admin vs Agent)
- [ ] Add AMC Radar widget
- [ ] Add TAT Monitor widget
- [ ] Implement file upload for attachments

## Tally Integration (TDL)
TDL plugin code is available in `tally/ticket_plugin.tdl` but is currently deprioritized.
