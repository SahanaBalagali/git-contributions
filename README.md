Git Contribution Tracker 📊
A lightweight command-line tool that tracks your git commits across all local repositories and displays them in a GitHub-style contribution graph right in your terminal.

Why This Tool? 🤔
GitHub's contribution graph only shows commits pushed to GitHub repositories. But what about all those commits in your local projects, private repos, or work repositories that use different platforms? This tool gives you the complete picture of your coding activity.

Features ✨
📈 GitHub-style contribution graph in your terminal
🔍 Scans and tracks commits from all your local git repositories
📅 Shows the last 6 months of activity
🎨 Color-coded cells based on commit frequency
📧 Filter commits by email address
🚀 Fast and lightweight

Installation 🛠️
Make sure you have Go installed on your system, then:
bashgit clone https://github.com/yourusername/git-contribution-tracker
cd git-contribution-tracker
go build -o git-tracker

Usage 🚀
First Time Setup
Before you can view your stats, you need to tell the tool which directories contain your git repositories:
bash./git-tracker -add /path/to/your/projects
./git-tracker -add /Users/yourname/Documents/code
./git-tracker -add /home/yourname/workspace
The tool will recursively scan these directories and find all git repositories.
View Your Contribution Graph
bash./git-tracker -email your@email.com
This will display a contribution graph showing your commit activity over the last 6 months.

Example Output 📋
         Mar Apr May Jun Jul Aug Sep 
 Mon   🟩 🟩 ⬜ 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩
 Wed   🟩 🟩 🟩 ⬜ 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩
 Fri   ⬜ 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩 🟩
 
How It Works 🔧
Scanning: The tool scans specified directories for .git folders
Storage: Repository paths are stored in ~/.gogitlocalstats
Analysis: When generating stats, it reads commit history from each repository
Filtering: Only commits matching your email address are counted
Visualization: Creates a color-coded grid showing commit frequency

Color Coding 🎨
⬜ Light gray: No commits
🟩 Light green: 1-3 commits
🟩 Medium green: 4-6 commits
🟩 Dark green: 7-10 commits
🟩 Darkest green: 10+ commits

Command Line Options 📝
OptionDescriptionExample-addAdd a directory to scan for repositories-add /path/to/projects-emailEmail address to filter commits by-email john@example.com
File Structure 📁
~/.gogitlocalstats    # Stores list of tracked repositories
Contributing 🤝
Feel free to submit issues and pull requests. Some ideas for future improvements:

Support for different time ranges (1 year, all time)
Export stats to different formats
Web interface
Team statistics

Acknowledgments 👏
Inspired by GitHub's contribution graph and the need to track all coding activity, not just what's on GitHub.
