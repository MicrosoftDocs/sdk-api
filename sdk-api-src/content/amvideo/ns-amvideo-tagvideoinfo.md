---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagVIDEOINFO structure


## -description



The <b>VIDEOINFO</b> structure is equivalent to a <a href="https://msdn.microsoft.com/a175592b-0dc1-4001-b52f-785407965932">VIDEOINFOHEADER</a> structure, but it contains enough memory to hold three color masks plus a color table with 256 colors.

If you are writing a video filter, you can use this structure to guarantee that the format block always has enough memory to contain the largest possible <a href="https://msdn.microsoft.com/a175592b-0dc1-4001-b52f-785407965932">VIDEOINFOHEADER</a> structure.




## -struct-fields




### -field rcSource


            Portion of the input video to use.
          


### -field rcTarget


            Where the video should be displayed.
          


### -field dwBitRate


            Approximate data rate in bits per second.
          


### -field dwBitErrorRate


            Bit error rate for this stream.
          


### -field AvgTimePerFrame


            The desired average time per frame, in 100-nanosecond units. For more information, see the Remarks section for the <a href="https://msdn.microsoft.com/a175592b-0dc1-4001-b52f-785407965932">VIDEOINFOHEADER</a> structure.
          


### -field bmiHeader


<a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure that contains color and dimension information for a device-independent bitmap.
          


### -field bmiColors


              Array of Win32 <a href="https://msdn.microsoft.com/22e0991d-078e-4b44-9f03-004137e31f6c">RGBQUAD</a> structures that specifies the video's color palette. Each structure represents a single color, which is a combination of red, green, and blue intensities.
            


### -field dwBitMasks


              Array of <b>DWORD</b> values that specify true-color bitmasks.
            


### -field TrueColorInfo


<a href="https://msdn.microsoft.com/8269d8c2-ff8e-48e0-b4f6-06900a7ecfdc">TRUECOLORINFO</a> structure that contains both a color palette and an array of color bitmasks.
            


## -remarks



Never use this structure unless you are sure that you will use it only to store standard RGB formats. If you store anything other than standard RGB, the variable size of the <b>bmiHeader</b> structure will almost certainly cause problems, and you should use the <a href="https://msdn.microsoft.com/a175592b-0dc1-4001-b52f-785407965932">VIDEOINFOHEADER</a> structure instead. If you find it absolutely necessary to use the <b>VIDEOINFO</b> structure, do not access the <b>TrueColorInfo</b>, <b>dwBitMasks</b>, or <b>bmiColors</b> members directly. Instead, use the <a href="https://msdn.microsoft.com/544e9ff2-186a-40d4-a0bd-d75e2091f268">TRUECOLOR</a>, <a href="https://msdn.microsoft.com/32541ee4-53ef-4f0a-b823-bb475a93a195">COLORS</a>, and <a href="https://msdn.microsoft.com/e90ddeab-a3d6-4d34-8608-4d8831d81fe5">BITMASKS</a> macros to return the pointers to the color information. Which of these members is valid depends on the contents of the <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure.

The first five data members are equivalent to a <a href="https://msdn.microsoft.com/a175592b-0dc1-4001-b52f-785407965932">VIDEOINFOHEADER</a> structure. They are expanded in full simply to reduce the amount of dereferencing needed when dealing with a pointer to a <b>VIDEOINFO</b> structure.

For information about using the <b>rcSource</b> and <b>rcTarget</b> members, see <a href="https://msdn.microsoft.com/fdddbffb-c44f-4364-9e2e-b721ba39c74f">Source and Target Rectangles in Video Renderers</a>.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

