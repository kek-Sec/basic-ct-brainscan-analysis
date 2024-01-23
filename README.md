# DICOM Image Processing Readme

This Python script processes DICOM images related to brain CT scans, utilizing the PyDicom library, Matplotlib, ITK, and other relevant tools. The code performs several tasks, including loading DICOM images, visualizing slices in a 4x4 plot, sorting images by instance number, converting them to a 3D array using ITK, correcting spacing and slice thickness, applying the Hounsfield scale, and calculating bone volume and mean HU values.

## Usage

1. **Load DICOM Images:**
   - The script loads DICOM images from the 'brain_ct_data' folder using PyDicom and creates a list of images.

2. **Visualize Slices:**
   - It visualizes slices 70 to 86 in a 4x4 plot using Matplotlib, both before and after sorting by instance number.

3. **Convert to 3D Array:**
   - The images are converted to a 3D array using ITK, and the 3D visualization is displayed.

4. **Correct Spacing and Slice Thickness:**
   - The script corrects spacing and slice thickness using ITK to enhance the accuracy of the visualization.

5. **Hounsfield Scale:**
   - It applies the Hounsfield scale formula (HU = Gray_Value * slope + intercept) to the images.

6. **Bone Volume Calculation:**
   - The script calculates the total volume of bone voxels based on a specified Hounsfield Unit (HU) range.

7. **Mean HU Calculation:**
   - It calculates the mean HU values for bone, white matter, and gray matter.

8. **White and Gray Matter Segmentation:**
   - It identifies white and gray matter based on HU thresholds and performs filtering for accurate segmentation.

9. **Visualization of Filtered Image:**
   - The final result is visualized using ITKWidgets after applying a filter to improve segmentation accuracy.

## Results

- **Bone Volume:**
  - The calculated bone volume is approximately 173.75 cubic millimeters.

- **Mean HU Values:**
  - Mean bone HU: 991.95
  - Mean white matter HU: 991.95
  - Mean gray matter HU: 0.0

## Notes

- The script uses various libraries for image processing, including PyDicom, Matplotlib, ITK, and SciPy.
- Careful attention is paid to correcting image spacing, slice thickness, and applying the Hounsfield scale for accurate medical image analysis.
