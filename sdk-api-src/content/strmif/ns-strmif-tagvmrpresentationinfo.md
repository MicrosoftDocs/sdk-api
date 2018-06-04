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

# tagVMRPRESENTATIONINFO structure


## -description



The <code>VMRPRESENTATIONINFO</code> structure is used in the <a href="https://msdn.microsoft.com/df6bf45d-df92-4655-862c-704a12a62ff9">IVMRImagePresenter::PresentImage</a> method (VMR-7 only).




## -struct-fields




### -field dwFlags

A bitwise combination of flags from the <a href="https://msdn.microsoft.com/27aab657-802e-4967-a5bd-3907637e1cfe">VMRPresentationFlags</a> enumeration, which describe the status of the video sample with respect to its presentation time.


### -field lpSurf

Pointer to the DirectDraw surface that contains the video frame to be presented.


### -field rtStart


            The start time for the current frame, in 100-nanosecond units.
          


### -field rtEnd


            The end time for the current frame, in 100-nanosecond units.
          


### -field szAspectRatio


            The aspect ratio of the rectangle.
          


### -field rcSrc


            The source rectangle.
          


### -field rcDst

The destination rectangle.
          


### -field dwTypeSpecificFlags

Bitwise combination of flags, as defined for the <b>dwTypeSpecificFlags</b> member of the <a href="https://msdn.microsoft.com/4fda7f64-130c-42c8-a671-2e24bdd0b09b">AM_SAMPLE2_PROPERTIES</a> structure.


### -field dwInterlaceFlags

Bitwise combination of flags, as defined for the <b>dwInterlaceFlags</b> member of the <a href="https://msdn.microsoft.com/5e3d5bf0-435f-45da-8409-a1463b56a7ae">VIDEOINFOHEADER2</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/5e3d5bf0-435f-45da-8409-a1463b56a7ae">VIDEOINFOHEADER2</a>
 

 

