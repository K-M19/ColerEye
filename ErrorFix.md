# Troubleshooting, Errors
### Error: "System.DllNotFoundException: Unable to load DLL 'ColerEyeDLL.dll': The specified module could not be found. (Exception from HRESULT: 0x8007007E)"
- You need the Visual C++ Redistributable for Visual Studio 2015.
- Make sure to take the x86 version, even if you have a x64 Windows.
- Download it here: https://www.microsoft.com/en-us/download/details.aspx?id=48145
- Or you can choose AIO for full library: https://www.techpowerup.com/download/visual-c-redistributable-runtime-package-all-in-one/

# Error: "ColerEyeProxy failed to initialize! Graphics card system type (Desktop / Laptop) is unknown!"
- Intel Laptops are not supported because there is no public API for their integrated GPU. ColerEye can not run on your laptop.
- NVIDIA laptops need to have the Digital ColerEye option in the NVIDIA Control Panel. If you do not have it, NVIDIA decided to disable Digital ColerEye for your mobile GPU. ColerEye can not run on your laptop.
- Did you recently switch your graphics card?
- Completely uninstall the old driver.
- Make sure you do not have leftovers from your previous driver:
- If you are now using AMD: remove/rename "nvapi.dll" file in your Windows folder.
- If you are now using NVIDIA: remove/rename "atiadlxx.dll" and "atiadlxy.dll" files in your Windows folder.
- Restart ColerEye

## Error: Screen gets a green tint when using AMD with a ColerEye value > 200
- The AMD algorithm tends to add green artifacts when setting the value > 200. This is due to how the algorithm calculates the visual output. Using a lower value should reduce green color artifacts.
- When you use 60 Hz, try forcing your Monitor to 75 Hz. A few users told me that this fixed their issue with greenish artifcats. Also switching between 4:3 and 16:9 resolutions might fix the green color artifacts.

  
## And "Update" Windows.
