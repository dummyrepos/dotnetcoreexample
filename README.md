# Weather Forecast API

A simple .NET 9 Web API that provides weather forecast data.

## Endpoints

### GET /weatherforecast
Returns a 5-day weather forecast with random temperature data.

**Response:**
```json
[
  {
    "date": "2024-01-15",
    "temperatureC": 25,
    "temperatureF": 77,
    "summary": "Warm"
  }
]
```

## Running the Application

1. **Prerequisites:**
   - .NET 9 SDK

2. **Run locally:**
   ```bash
   dotnet run
   ```

3. **Access the API:**
   - Development: `https://localhost:5001/weatherforecast`
   - OpenAPI documentation: `https://localhost:5001/openapi/v1.json` (Development only)

## Usage Examples

### cURL
```bash
curl https://localhost:5001/weatherforecast
```

### PowerShell
```powershell
Invoke-RestMethod -Uri "https://localhost:5001/weatherforecast"
```

## Response Format

Each forecast item contains:
- `date`: Date in YYYY-MM-DD format
- `temperatureC`: Temperature in Celsius (-20 to 55)
- `temperatureF`: Temperature in Fahrenheit (calculated)
- `summary`: Weather description (Freezing, Bracing, Chilly, Cool, Mild, Warm, Balmy, Hot, Sweltering, Scorching)