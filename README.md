# Place Finder Android App

A comprehensive Android application that allows users to search for places worldwide and get detailed information including pincode/postal codes.

## Features

- 🔍 **Global Place Search**: Search for any place worldwide using text input
- 📍 **Current Location**: Get details about your current location including pincode
- 🗺️ **Detailed Information**: View comprehensive place details including:
  - Place name and address
  - Pincode/Postal code
  - GPS coordinates
  - Place type (city, town, village, etc.)
- 🎯 **Interactive Results**: Click on search results to view detailed information
- 🎨 **Modern UI**: Clean Material Design interface with proper error handling
- ⚡ **Real-time Search**: Debounced search with loading indicators
- 🔐 **Permission Management**: Smart location permission handling

## Technical Architecture

### Architecture Pattern
- **MVVM (Model-View-ViewModel)**: Clean architecture separation
- **Repository Pattern**: Centralized data management
- **LiveData & Flow**: Reactive programming for UI updates

### Key Technologies
- **Kotlin**: Modern Android development language
- **Retrofit**: HTTP client for API communications
- **OpenStreetMap Nominatim API**: Free geocoding service
- **Google Play Services**: Location services
- **Material Design Components**: Modern UI components
- **Coroutines**: Asynchronous programming
- **ViewBinding**: Type-safe view references
- **Dexter**: Simplified permission handling

### API Integration
- **Nominatim API**: OpenStreetMap's free geocoding service
  - Search places by text query
  - Reverse geocoding from coordinates
  - No API key required
  - Supports worldwide locations

## Project Structure

```
app/src/main/java/com/placefinder/
├── data/
│   ├── api/
│   │   ├── ApiClient.kt              # Retrofit configuration
│   │   └── NominatimApiService.kt    # API service interface
│   ├── model/
│   │   ├── Place.kt                  # Place data model
│   │   └── ApiResponse.kt            # Response wrapper classes
│   └── repository/
│       ├── PlaceRepository.kt        # Repository interface
│       └── PlaceRepositoryImpl.kt    # Repository implementation
├── ui/main/
│   ├── MainActivity.kt               # Main screen activity
│   ├── MainViewModel.kt              # Business logic
│   ├── MainViewModelFactory.kt       # ViewModel factory
│   └── PlacesAdapter.kt              # RecyclerView adapter
└── utils/                            # Utility classes
```

## Setup Instructions

1. **Clone/Download** the project to your local machine
2. **Open** the project in Android Studio
3. **Sync** the project to download dependencies
4. **Build** and **Run** the application on a device/emulator

### Requirements
- Android Studio Arctic Fox or later
- Android SDK 24 (Android 7.0) or higher
- Internet connection for place search
- Location services for current location feature

## Permissions

The app requires the following permissions:

- `INTERNET`: For API calls to search places
- `ACCESS_NETWORK_STATE`: To check network connectivity
- `ACCESS_FINE_LOCATION`: For precise location access
- `ACCESS_COARSE_LOCATION`: For approximate location access

## How to Use

1. **Search Places**: 
   - Type in the search bar to find places worldwide
   - Results appear automatically as you type
   - Tap on any result to view detailed information

2. **Current Location**:
   - Tap "Use Current Location" button
   - Grant location permissions when prompted
   - View your current location details including pincode

3. **View Details**:
   - Selected places show comprehensive information
   - Includes formatted address, pincode, and coordinates
   - Error messages appear for any issues

## API Information

This app uses the **Nominatim API** by OpenStreetMap:
- **Base URL**: `https://nominatim.openstreetmap.org/`
- **Documentation**: https://nominatim.org/release-docs/latest/api/Overview/
- **Rate Limits**: Please be respectful with usage
- **Attribution**: Data © OpenStreetMap contributors

## Error Handling

The app includes comprehensive error handling for:
- Network connectivity issues
- API failures and timeouts
- Location permission denials
- Invalid search queries
- GPS/location service errors

## Future Enhancements

Potential improvements for the app:
- Place photos integration
- Favorite places storage
- Map view integration
- Offline caching of recent searches
- Multiple language support
- Place categories and filtering

## License

This project is created for educational purposes. Please respect OpenStreetMap's usage policies when using their Nominatim API.

## Contributing

Feel free to fork this project and submit pull requests for any improvements or bug fixes.
