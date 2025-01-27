# Orderbook

A high-performance C++ orderbook implementation supporting multiple order types and matching algorithms.

## Features

- Multiple order types support:
  - Good Till Cancel (GTC)
  - Fill And Kill (FAK)
  - Fill Or Kill (FOK)
  - Good For Day (GFD)
  - Market Orders

- Thread-safe operations with mutex protection
- Automatic pruning of Good For Day orders at market close (16:00)
- Price-time priority matching algorithm
- Support for both buy and sell orders
- Real-time level data tracking
- Order modification capabilities

## Order Types

### Good Till Cancel (GTC)
Orders that remain in the book until explicitly cancelled or fully matched.

### Fill And Kill (FAK)
Orders that get filled for available quantity and cancel remaining amount.

### Fill Or Kill (FOK)
Orders that must be filled completely or cancelled entirely.

### Good For Day (GFD)
Orders that automatically get cancelled at market close (16:00).

### Market Orders
Orders that match at the best available price.

## Core Components

The implementation consists of several key components:

1. **Orderbook**: Main matching engine implementation
2. **Order**: Base order representation
3. **Trade**: Matched trade information
4. **LevelInfo**: Price level aggregation