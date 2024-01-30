# LinkedIn Profile Information Retrieval Script

## Overview

This Python script is designed to retrieve information about LinkedIn companies using their slugs. It makes use of the Piloterr API to fetch data and stores the results in a JSON file. The script utilizes concurrent programming for efficient processing and includes error handling mechanisms to handle HTTP and request errors.

## Prerequisites

Before running the script, make sure to set up the following:

- Python environment
- Required Python packages: `dotenv`, `requests`, `tqdm`, `termcolor`
- API Token: Obtain an API token from Piloterr and set it in the `.env` file.

## Usage

1. Install the required packages:

```bash
pip install dotenv requests tqdm termcolor
```

2. Set up the API token:

- Create a `.env` file in the script directory.
- Add the following line with your Piloterr API token:

```plaintext
API_TOKEN=your_api_token_here
```

- Change the `MAX_WORKERS` variable in the script to set the number of concurrent workers.
- Save the file.

3. Prepare the CSV file:

- Create a CSV file named `extract.csv` with a column containing LinkedIn profile slugs.

4. Run the script:

```bash
python linkedin_profile.py
```

## Results

The script outputs the retrieved profile information in a JSON file named `results.json`.

```json
{
  "https://www.linkedin.com/in/satyanadella": {
    "address": {
      "city": "Redmond",
      "state": "Washington",
      "county": "King County",
      "country": "United States",
      "country_code": "US"
    },
    "summary": "As chairman and CEO of Microsoft, I define my mission and that of my company as…",
    "articles": [
      {
        "url": "https://www.linkedin.com/pulse/age-copilots-satya-nadella-2hllc",
        "title": "The age of copilots",
        "author": "Satya Nadella"
      },
      {
        "url": "https://www.linkedin.com/pulse/my-annual-letter-leading-new-era-satya-nadella",
        "title": "My annual letter: Leading in a new era",
        "author": "Satya Nadella"
      },
      {
        "url": "https://www.linkedin.com/pulse/creating-new-opportunity-across-our-partner-ecosystem-satya-nadella",
        "title": "Creating new opportunity across our partner ecosystem in this AI era",
        "author": "Satya Nadella"
      },
      {
        "url": "https://www.linkedin.com/pulse/5-new-developer-opportunities-ai-era-satya-nadella",
        "title": "5 new developer opportunities in this AI era",
        "author": "Satya Nadella"
      }
    ],
    "headline": null,
    "username": "satyanadella",
    "full_name": "Satya Nadella",
    "languages": [],
    "photo_url": "https://media.licdn.com/dms/image/C5603AQHHUuOSlRVA1w/profile-displayphoto-shrink_200_200/0/1579726625398?e=2147483647&v=beta&t=if0cGPpfDtj9RXsBa0E7yQVAFE5G_wgfyxLxol32STo",
    "activities": [],
    "educations": [
      {
        "end_at": "1996-01-30 00:00:00",
        "school": "The University of Chicago Booth School of Business",
        "address": null,
        "location": null,
        "start_at": "1994-01-30 00:00:00",
        "school_url": "https://www.linkedin.com/school/universityofchicagoboothschoolofbusiness/",
        "description": null
      }
    ],
    "experiences": [
      {
        "address": null,
        "company": "The University of Chicago Booth School of Business",
        "end_date": "1996-01-30 00:00:00",
        "location": null,
        "start_at": "1994-01-30 00:00:00",
        "company_url": "https://www.linkedin.com/school/universityofchicagoboothschoolofbusiness/",
        "description": null
      }
    ],
    "profile_url": "https://www.linkedin.com/in/satyanadella",
    "website_url": "http://www.microsoft.com/ceo",
    "background_url": "https://media.licdn.com/dms/image/C5616AQHEITsxuRUzWw/profile-displaybackgroundimage-shrink_200_800/0/1553288711074?e=2147483647&v=beta&t=G53pten0y8URG3V3hscyH-1sXVlkD9GTtiNJySH0qhU",
    "follower_count": 10722458,
    "recommendations": [],
    "section_courses": [],
    "section_patents": [],
    "connection_count": null,
    "section_projects": [],
    "people_also_viewed": [
      {
        "url": "https://www.linkedin.com/in/williamhgates",
        "name": "Bill Gates",
        "summary": null,
        "location": "Seattle, WA"
      },
      {
        "url": "https://in.linkedin.com/in/aman-gupta-7217a515",
        "name": "Aman Gupta",
        "summary": null,
        "location": "Delhi, India"
      },
      {
        "url": "https://in.linkedin.com/in/narendramodi",
        "name": "Narendra Modi",
        "summary": null,
        "location": "Delhi, India"
      },
      {
        "url": "https://www.linkedin.com/in/clarashih",
        "name": "Clara Shih",
        "summary": null,
        "location": "San Francisco, CA"
      },
      {
        "url": "https://www.linkedin.com/in/jane-fraser-3292068",
        "name": "Jane Fraser",
        "summary": null,
        "location": "New York, NY"
      },
      {
        "url": "https://www.linkedin.com/in/ryanroslansky",
        "name": "Ryan Roslansky",
        "summary": null,
        "location": "San Francisco Bay Area"
      },
      {
        "url": "https://in.linkedin.com/in/vineetasingh",
        "name": "Vineeta Singh",
        "summary": null,
        "location": "Mumbai"
      },
      {
        "url": "https://www.linkedin.com/in/parag-agrawal-5a14742a",
        "name": "Parag Agrawal",
        "summary": null,
        "location": "San Francisco, CA"
      },
      {
        "url": "https://in.linkedin.com/in/rajeshgopinathan",
        "name": "Rajesh Gopinathan",
        "summary": null,
        "location": "Mumbai"
      },
      {
        "url": "https://www.linkedin.com/in/jamiedimon",
        "name": "Jamie Dimon",
        "summary": null,
        "location": "New York, NY"
      },
      {
        "url": "https://www.linkedin.com/in/jeffweiner08",
        "name": "Jeff Weiner",
        "summary": null,
        "location": "United States"
      },
      {
        "url": "https://www.linkedin.com/in/guthriescott",
        "name": "Scott Guthrie",
        "summary": null,
        "location": "Bellevue, WA"
      },
      {
        "url": "https://ca.linkedin.com/in/dave-mckay-4189071",
        "name": "Dave McKay",
        "summary": null,
        "location": "Toronto, ON"
      },
      {
        "url": "https://www.linkedin.com/in/dougmcmillon",
        "name": "Doug McMillon",
        "summary": null,
        "location": "Bentonville, AR"
      },
      {
        "url": "https://www.linkedin.com/in/rbranson",
        "name": "Richard Branson",
        "summary": null,
        "location": null
      },
      {
        "url": "https://www.linkedin.com/in/anjalisud",
        "name": "Anjali Sud",
        "summary": null,
        "location": "New York, NY"
      },
      {
        "url": "https://www.linkedin.com/in/david-m-solomon",
        "name": "David Solomon",
        "summary": null,
        "location": "New York, NY"
      },
      {
        "url": "https://www.linkedin.com/in/reedhastings",
        "name": "Reed Hastings",
        "summary": null,
        "location": "Los Gatos, CA"
      },
      {
        "url": "https://www.linkedin.com/in/ariannahuffington",
        "name": "Arianna Huffington",
        "summary": null,
        "location": "New York, NY"
      },
      {
        "url": "https://in.linkedin.com/in/shradha-khapra",
        "name": "Shradha Khapra",
        "summary": null,
        "location": "Delhi, India"
      }
    ],
    "section_test_scores": [],
    "section_publications": [],
    "card_current_position": {
      "url": "https://www.linkedin.com/company/microsoft",
      "name": "Microsoft"
    },
    "section_honors_awards": [],
    "section_organizations": [],
    "card_current_education": {
      "url": "https://www.linkedin.com/school/universityofchicagoboothschoolofbusiness/",
      "name": "The University of Chicago Booth School of Business"
    },
    "section_certifications": [],
    "section_volunteer_experiences": []
  },
  "https://www.linkedin.com/in/williamhgates": {
    "address": {
      "city": "Seattle",
      "state": "Washington",
      "county": "King County",
      "country": "United States",
      "country_code": "US"
    },
    "summary": "Co-chair of the Bill & Melinda Gates Foundation. Founder of Breakthrough Energy…",
    "articles": [
      {
        "url": "https://www.linkedin.com/pulse/2024-elections-shape-future-global-health-climate-bill-gates-1pwfc",
        "title": "2024 elections will shape the future of global health and the climate",
        "author": "Bill Gates"
      },
      {
        "url": "https://www.linkedin.com/pulse/long-awaited-malnutrition-breakthrough-almost-here-bill-gates-fpgxc",
        "title": "A long-awaited malnutrition breakthrough is almost here.",
        "author": "Bill Gates"
      },
      {
        "url": "https://www.linkedin.com/pulse/ai-supercharge-innovation-pipeline-bill-gates-rsmqc",
        "title": "AI is about to supercharge the innovation pipeline",
        "author": "Bill Gates"
      },
      {
        "url": "https://www.linkedin.com/pulse/year-signaled-start-new-era-bill-gates-qbpfc",
        "title": "This year signaled the start of a new era",
        "author": "Bill Gates"
      }
    ],
    "headline": null,
    "username": "williamhgates",
    "full_name": "Bill Gates",
    "languages": [],
    "photo_url": "https://media.licdn.com/dms/image/D5603AQHv6LsdiUg1kw/profile-displayphoto-shrink_200_200/0/1695167344576?e=2147483647&v=beta&t=XAUf_Aqfa5tAmMqvOXPJ26wXV73tOHvI-rygpb_WpQA",
    "activities": [],
    "educations": [
      {
        "end_at": "1975-01-30 00:00:00",
        "school": "Harvard University",
        "address": null,
        "location": null,
        "start_at": "1973-01-30 00:00:00",
        "school_url": "https://www.linkedin.com/school/harvard-university/",
        "description": null
      }
    ],
    "experiences": [
      {
        "address": null,
        "company": "Harvard University",
        "end_date": "1975-01-30 00:00:00",
        "location": null,
        "start_at": "1973-01-30 00:00:00",
        "company_url": "https://www.linkedin.com/school/harvard-university/",
        "description": null
      }
    ],
    "profile_url": "https://www.linkedin.com/in/williamhgates",
    "website_url": "https://gatesnot.es/UnconfuseMe",
    "background_url": "https://media.licdn.com/dms/image/D5616AQHy2R5tyt2YUA/profile-displaybackgroundimage-shrink_200_800/0/1672782785474?e=2147483647&v=beta&t=RTQAJraPOkiQsVFiZcawowadxaryw7iRq9Bgmy2L_go",
    "follower_count": 35036886,
    "recommendations": [],
    "section_courses": [],
    "section_patents": [],
    "connection_count": null,
    "section_projects": [],
    "people_also_viewed": [],
    "section_test_scores": [],
    "section_publications": [],
    "card_current_position": {
      "url": "https://www.linkedin.com/company/bill-&-melinda-gates-foundation",
      "name": "Bill & Melinda Gates Foundation"
    },
    "section_honors_awards": [],
    "section_organizations": [],
    "card_current_education": {
      "url": "https://www.linkedin.com/school/harvard-university/",
      "name": "Harvard University"
    },
    "section_certifications": [],
    "section_volunteer_experiences": []
  }
}
```

Additionally, it maintains a record of failed rows in `failed_rows.txt` for reprocessing in subsequent runs.

## Contributing

Feel free to contribute by submitting issues or pull requests. Your feedback and improvements are welcome!