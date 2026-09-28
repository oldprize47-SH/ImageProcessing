# Image Processing Labs

These are my assignments and exercises from the 2025 image-processing course. They include C++/OpenCV programs, notebooks, test images and course-provided helper code.

The lane-detection assignment is one example. The program processes a road image and marks the lane centre. Its source is in [the lane-detection assignment](Assignment/Assignment_Line_Detection/DLIP_Assignment_21800275_SangheonPark.cpp).

![Recorded output of the lane-detection assignment](Assignment/Assignment_Line_Detection/Lane_center.jpg)

This image is a saved result from the assignment, not a new benchmark run.

The local versions of the [gear-detection lab](LAB/DLIP_LAB1/DLIP_LAB1_21800275_SangheonPark.cpp) and [steel-strip shape lab](LAB/DLIP_LAB3/DLIP_LAB3_21800275_SangheonPark_image.py) were incorporated on 28 September 2026. The Python file passed a syntax check; no new image-processing benchmark was run.

## What the assignments do

The [gear inspection lab](LAB/DLIP_LAB1/DLIP_LAB1_21800275_SangheonPark.cpp) uses thresholding, morphology and contours to separate the gear teeth and identify unusual tooth areas. The exercise connects a visible defect with a geometric feature that can be measured in the image. Its saved examples are not a benchmark across all gear shapes or lighting conditions.

The [colour-masking lab](LAB/DLIP_LAB2/DLIP_LAB2_21800275_SangheonPark_sample1.cpp) creates an invisibility-cloak effect. It selects a colour range in HSV space, refines the mask and replaces the selected part of the current frame with a background image. Lighting and the separation between foreground and background colours affect the result.

The [steel-strip shape lab](LAB/DLIP_LAB3/DLIP_LAB3_21800275_SangheonPark_image.py) extracts edges from an image, suppresses unwanted structure and fits a quadratic curve to the remaining boundary points. It derives a displayed level from the curve's position in the image. That level is an image-based score, not a calibrated measurement of physical tension or stress.

The lane assignment uses Canny edges, a region of interest and Hough lines to select left and right lane candidates. It forms representative lines and solves for their intersection to show a vanishing point and driving region. The report's examples are still images; this does not demonstrate a vehicle-control system or stable detection over a complete driving video.

## Reading and reproducing an exercise

Start with the lane source and the saved image above: identify the input, then follow edge extraction, line selection and the final overlay. For the other labs, compare the image-processing stages with the files in their own lab folders. The filenames and course helper code are retained to keep the connection with the original assignments.

Before running a file, check its input-image path, working directory and output locations. Several exercises were developed as individual Windows projects rather than as one installable package. Python exercises need their imported numerical/image-processing packages; C++ exercises need the OpenCV headers and libraries configured for the chosen compiler.

## Building

The [OpenCV property sheet](Props/opencv-4.11.0_release_x64.props) records the original Windows/OpenCV 4.11 setup. Library paths need to be adjusted for another machine. A full rebuild has not been performed during this documentation update.

[Include/TU_DLIP.cpp](Include/TU_DLIP.cpp) contains course helper functions. The repository includes supplied teaching material as well as my coursework; those sources keep their original attribution.

The final [Gaze Tracking Mouse project](https://github.com/oldprize47-SH/gaze-mouse-course-project) is documented separately.

[Original repository](https://github.com/oldprize47/DLIP_2025). Original history and attribution are retained.
