# ISBN Data Extraction from PPDVN Registry

A scraper that queries the PPDVN.gov.vn publishing registry to retrieve ISBNs based on book titles and publishers.

A client maintains several tables containing book metadata, including book titles, publishers, and publishing years. However, all entries are missing ISBN numbers, as ISBN registration has historically not been a widely adopted practice in parts of the Vietnamese publishing industry.

To complete the dataset, the client initially planned to hire multiple people to manually search for ISBN numbers on the official website of the Vietnam Publication Department at <a href='https://ppdvn.gov.vn/'>ppdvn.gov.vn</a>, where publishers register books with ISBNs. Unfortunately, the website is frequently unavailable and often returns 503 errors, making manual lookup inefficient and unreliable.

To address this problem, I proposed an automated data pipeline that:

- Scrapes the website by publisher and publication year
- Extracts relevant metadata, including ISBN, book titles, and publishers
- Cleans and structures the extracted data
- Merges the results back into the client's original tables to populate the missing ISBN fields

This approach significantly reduces manual effort and creates a scalable process for enriching the dataset with ISBN information.
