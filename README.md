# Mobile Banking App

This is a simple Flutter-based Mobile Banking App that lets users view their accounts, check transaction histories, and perform basic banking operations like deposits and withdrawals.

## Features

- **Welcome Screen**: Displays a greeting and the current date.
- **Account List**: Shows available accounts with their balances.
- **Transaction History**: Lets users see transactions for selected accounts.

---

## Installation

1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/mobile-banking-app.git
Install dependencies:

bash
Copy
Edit
flutter pub get
Run the app:

bash
Copy
Edit
flutter run
Code Overview
lib/main.dart: Main app entry point and routes setup.
lib/screens/welcome_screen.dart: Displays the welcome message and navigates to the account list.
lib/screens/account_list_screen.dart: Shows accounts and balances using a dynamic list.
lib/screens/transaction_details_screen.dart: Displays transaction details for a selected account.
Code Example
In welcome_screen.dart, the welcome message and navigation are handled as follows:

dart
Copy
Edit
ElevatedButton(
  onPressed: () {
    Navigator.push(
      context,
      MaterialPageRoute(builder: (context) => AccountListScreen()),
    );
  },
  child: Text('View Accounts'),
);
In account_list_screen.dart, accounts are listed dynamically:

dart
Copy
Edit
ListView.builder(
  itemCount: accounts.length,
  itemBuilder: (context, index) {
    return ListTile(
      title: Text(accounts[index]['name']),
      subtitle: Text('Balance: \$${accounts[index]['balance']}'),
    );
  },
);
AI Contributions
Some parts of the code were generated with AI tools, particularly for UI components and routing.

Future Enhancements
API Integration: Fetch real data from a server.
User Authentication: Add login functionality.
UI Improvements: Enhance the design and animations.
