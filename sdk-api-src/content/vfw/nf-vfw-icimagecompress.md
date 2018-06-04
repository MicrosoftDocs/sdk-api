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

# ICImageCompress function


## -description



The <b>ICImageCompress</b> function compresses an image to a given size. This function does not require initialization functions.




## -parameters




### -param hic


            Handle to a compressor opened with the <a href="https://msdn.microsoft.com/2637b6ef-2324-40db-99e4-773fcb6fdbf6">ICOpen</a> function. Specify <b>NULL</b> to have VCM select an appropriate compressor for the compression format. An application can have the user select the compressor by using the <a href="https://msdn.microsoft.com/4a58df6a-9ac4-44bb-8c49-338bb60193fc">ICCompressorChoose</a> function, which opens the selected compressor and returns a handle of the compressor in this parameter.
          


### -param uiFlags


            Reserved; must be zero.
          


### -param lpbiIn


            Pointer to the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the input data format.
          


### -param lpBits


            Pointer to input data bits to compress. The data bits exclude header and format information.
          


### -param lpbiOut


            Pointer to the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the compressed output format. Specify <b>NULL</b> to have the compressor use an appropriate format.
          


### -param lQuality


            Quality value used by the compressor. Values range from 0 to 10,000.
          


### -param plSize


            Maximum size desired for the compressed image. The compressor might not be able to compress the data to fit within this size. When the function returns, this parameter points to the size of the compressed image. Image sizes are specified in bytes.
          


## -returns




            Returns a handle to a compressed DIB. The image data follows the format header.
          




## -remarks



To obtain the format information from the <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure, use the <a href="http://go.microsoft.com/fwlink/p/?linkid=17081">GlobalLock</a> function to lock the data. Use the <a href="http://go.microsoft.com/fwlink/p/?linkid=17082">GlobalFree</a> function to free the DIB when you are finished.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

