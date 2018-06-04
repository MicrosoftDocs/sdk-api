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

# tagBITMAPFILEHEADER structure


## -description



The <b>BITMAPFILEHEADER</b> structure contains information about the type, size, and layout of a file that contains a DIB.




## -struct-fields




### -field bfType

The file type; must be BM.


### -field bfSize

The size, in bytes, of the bitmap file.


### -field bfReserved1

Reserved; must be zero.


### -field bfReserved2

Reserved; must be zero.


### -field bfOffBits

The offset, in bytes, from the beginning of the <b>BITMAPFILEHEADER</b> structure to the bitmap bits.


## -remarks



A <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> or <a href="https://msdn.microsoft.com/cb6cb9da-8f7f-47e9-980a-aa77fe04c80c">BITMAPCOREINFO</a> structure immediately follows the <b>BITMAPFILEHEADER</b> structure in the DIB file. For more information, see <a href="https://msdn.microsoft.com/44f19d14-4e0e-4512-8c86-6bd34ca4e87b">Bitmap Storage</a>.




## -see-also




<a href="https://msdn.microsoft.com/cb6cb9da-8f7f-47e9-980a-aa77fe04c80c">BITMAPCOREINFO</a>



<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>
 

 

