---
UID: NS:magnification.tagMAGIMAGEHEADER
title: MAGIMAGEHEADER
author: windows-sdk-content
description: Describes an image format.
old-location: magapi\magapi_magimageheader.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\structures\magimageheaderstruct.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMAGIMAGEHEADER, MAGIMAGEHEADER, MAGIMAGEHEADER structure [Magnification API], PMAGIMAGEHEADER, PMAGIMAGEHEADER structure pointer [Magnification API], magapi.magapi_magimageheader, magapi_magimageheader, magnification/MAGIMAGEHEADER, magnification/PMAGIMAGEHEADER"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: magnification.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Magnification.h
api_name:
 - MAGIMAGEHEADER
product: Windows
targetos: Windows
req.typenames: MAGIMAGEHEADER, *PMAGIMAGEHEADER
req.redist: 
---

# MAGIMAGEHEADER structure


## -description


<div class="alert"><b>Note</b>  The <b>MAGIMAGEHEADER</b> structure is deprecated in Windows 7 and later, and should not be used in new applications.  There is no alternate functionality.</div><div> </div>Describes an image format.


## -struct-fields




### -field width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The width of the image.


### -field height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The height of the image.


### -field format

Type: <b>WICPixelFormatGUID</b>

A WICPixelFormatGUID (declared in wincodec.h) that specifies the pixel format of the image. For a list of available pixel formats, see the <a href="https://msdn.microsoft.com/348b6d15-e339-4dce-99f3-4d639ee9bf7d">Native Pixel Formats</a> topic.



### -field stride

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The stride, or number of bytes in a row of the image.


### -field offset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The offset of the start of the image data from the beginning of the file.


### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

The size of the data.


## -see-also




<a href="https://msdn.microsoft.com/9452fe5d-d8e9-4953-b55b-7bf792cabe16">MagImageScalingCallback</a>
 

 

