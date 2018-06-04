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

# ICGetDisplayFormat function


## -description



The <b>ICGetDisplayFormat</b> function determines the best format available for displaying a compressed image. The function also opens a compressor if a handle of an open compressor is not specified.




## -parameters




### -param hic


            Handle to the compressor to use. Specify <b>NULL</b> to have VCM select and open an appropriate compressor.
          


### -param lpbiIn


            Pointer to <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the compressed format.
          


### -param lpbiOut


            Pointer to a buffer to return the decompressed format. The buffer should be large enough for a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure and 256 color entries.
          


### -param BitDepth


            Preferred bit depth, if nonzero.
          


### -param dx


            Width multiplier to stretch the image. If this parameter is zero, that dimension is not stretched.
          


### -param dy


            Height multiplier to stretch the image. If this parameter is zero, that dimension is not stretched.
          


## -returns




            Returns a handle to a decompressor if successful or zero otherwise.
          




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

