# test-font-issue-angular-cli-1.7.0-rc.0
The repository contains vanilla project generated by angular CLI 1.7.0-rc.0

After upgrading angular-cli from "1.6.3" to "1.7.0-rc.0" fonts are corrupted when build is executed
1) yarn
2) ng serve
3) Open the page on localhost:4200
4) Check logs, and you will see:

Failed to decode downloaded font: http://localhost:4200/fontawesome-webfont.68560c510686599ffbc9.woff2?v=4.7.0
localhost/:1 OTS parsing error: Failed to convert WOFF 2.0 font to SFNT
localhost/:1 Failed to decode downloaded font: http://localhost:4200/fontawesome-webfont.a7bbeb589ae63e018872.woff?v=4.7.0
localhost/:1 OTS parsing error: incorrect file size in WOFF header
localhost/:1 Failed to decode downloaded font: http://localhost:4200/fontawesome-webfont.e1dd9adb4f69bb9a0bdc.ttf?v=4.7.0
localhost/:1 OTS parsing error: incorrect entrySelector for table directory
localhost/:1 Failed to decode downloaded font: http://localhost:4200/fontawesome-webfont.912ec66d7572ff821749.svg?v=4.7.0#fontawesomeregular
localhost/:1 OTS parsing error: invalid version tag

Checking of mentioned before fonts shows that they are really corrupted and have different size than original fonts from the catalog node_modules/font-awesome/fonts/
