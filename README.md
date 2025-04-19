import requests

def scan_headers(url):
    try:
        # Web sitesine GET isteği gönder
        response = requests.get(url)

        # Headerları ekrana yazdır
        print(f"URL: {url}")
        print("HTTP Headers:")
        for header, value in response.headers.items():
            print(f"{header}: {value}")
    
    except requests.exceptions.RequestException as e:
        print(f"Bir hata oluştu: {e}")

# Kullanıcıdan URL al
if __name__ == "__main__":
    url = input("Target URL (örn. https://example.com): ")
    scan_headers(url)
