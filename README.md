
<div align="center">
  <img width="70%" src="assets/gitraptor_logo.png" />
  <h1>GitRaptor v1.0.0</h1>
  <br/>

  <p><i>GitRaptor is a powerful and automated tool for recovering and reconstructing Git repositories from exposed `.git` directories.</i></p>
  <br />

  <img src="assets/demo.gif" width="90%" /><br />
</div>

> :warning: **GitRaptor is a tool for ethical purposes only.** It is intended to help developers secure their systems by identifying potential misconfigurations. Unauthorized usage is strictly prohibited.

---

### Features

#### Key Capabilities
- Automated detection of `.git` files on a target URL
- Excludes specified file types for customized execution
- Recursive reconstruction of Git repositories
- Supports both `git-dumper` and manual fallback methods
- SSL/TLS validation bypass (optional)
- Follows HTTP redirections for more complex configurations
- Verbose mode for detailed execution logs

#### Supported Platforms
- Linux (Debian, Ubuntu, Kali)
- macOS (with additional dependencies)
- Windows (via WSL)

---

### Quick Start

1. **Download the Latest Release**
   Visit the [Releases Page](https://github.com/wezoomagency/GitRaptor/releases/download/v1.0.0/gitraptor-v1.0.0-amd64.tar.gz) to download the latest version of GitRaptor for your platform.

2. **Run GitRaptor**
   After downloading the binary, make it executable and run it:

   ```bash
   chmod +x gitraptor
   ./gitraptor -u <TARGET_URL> -e <EXCLUDE_EXTENSIONS> -k -r -v <DIRECTORY>
   ```

   Example:
   ```bash
   ./gitraptor -u https://example.com/.git -e "log,swp" -k -v ~/recovered_repo
   ```

---

### Command-Line Options

| Flag             | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| `-u`             | Target URL for the exposed `.git` directory (required).                   |
| `-e`             | Comma-separated list of file extensions to exclude (optional).            |
| `-k`             | Ignore SSL certificate validation (optional).                             |
| `-r`             | Follow HTTP redirections (optional).                                       |
| `-v`             | Enable verbose output (optional).                                          |
| `<DIRECTORY>`    | Local directory for saving reconstructed repository (required).           |

---

#### Comparison: GitRaptor vs. Git-Dumper

The image above demonstrates a direct comparison between **GitRaptor** and the widely-used **Git-Dumper** tool:

<a target="_blank" rel="noopener noreferrer" href="https://youtu.be/eob10kEgXu8"><img src="assets/comparison.jpg" width="90%" /></a>

- **GitRaptor**:
  - **Total size extracted**: 580
  - **Files extracted**: Includes `.git`, multiple JavaScript files, and `bitbucket-pipelines.yml`.
  - **Result**: Comprehensive extraction with a wide range of critical files, making it highly effective for analysis.

- **Git-Dumper**:
  - **Total size extracted**: 16
  - **Files extracted**: Limited to `.git` and `bitbucket-pipelines.yml`.
  - **Result**: Minimal valuable content, showing limited extraction capabilities.

This comparison highlights GitRaptor's efficiency and thoroughness in extracting critical files, making it a superior choice for analysis and recovery.

### Recognition

Even before its official release, **GitRaptor** has caught the attention of leading cybersecurity platforms.

> <a target="_blank" rel="noopener noreferrer" href="https://www.linkedin.com/feed/update/urn:li:activity:7281216516333690880?commentUrn=urn%3Ali%3Acomment%3A%28activity%3A7281216516333690880%2C7282463242625368065%29&dashCommentUrn=urn%3Ali%3Afsd_comment%3A%287282463242625368065%2Curn%3Ali%3Aactivity%3A7281216516333690880%29"><img src="assets/thn.png" width="90%" /></a>

### Community

You can join the official [GitRaptor Discord](https://discord.gg/sJM7rPPj) to chat with the community! 

### Contributing

To contribute to the GitRaptor tool, please review the guidelines in [Contributing.md](CONTRIBUTING.md) and then open a pull-request! 

### Note

GitRaptor has been created as an automated tool for recovering and reconstructing Git repositories from exposed `.git` directories. On certain targets, it may behave unexpectedly, such as downloading a PHP page with HTML content. 

Please note that this is the first version, and we are working daily to improve it.

### Disclaimer

**GitRaptor is a security tool intended for ethical use only.** Unauthorized use against systems without explicit permission is a violation of laws and ethical guidelines.

### Sponsors

[Wezoom](https://wezoom.ca) has sponsored this project by supporting GitRaptor's development and growth.

<img width="400" src="assets/wezoom_logo.png" alt="Wezoom logo.">

