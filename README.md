git clone https://github.com/pjsip/pjproject.git

git log -S "alsa_dev" > alsa_dev.commit

git checkout 19a87c7a0

git diff HEAD~ HEAD > alsa_dev.patch

git diff HEAD~ HEAD --name-only > alsa_dev.1

git diff HEAD~ HEAD --name-only | xargs zip update.zip
