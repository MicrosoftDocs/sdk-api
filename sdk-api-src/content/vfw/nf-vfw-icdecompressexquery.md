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

# ICDecompressExQuery function


## -description



The <b>ICDecompressExQuery</b> function determines if a decompressor can decompress data with a specific format.




## -parameters




### -param hic

Handle to the decompressor to use.


### -param dwFlags

Reserved; do not use.


### -param lpbiSrc

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the format of the compressed data to decompress.


### -param lpSrc

Reserved; must be <b>NULL</b>.


### -param xSrc

The x-coordinate of the source rectangle for the DIB specified by <i>lpbiSrc</i>.


### -param ySrc

The y-coordinate of the source rectangle for the DIB specified by <i>lpbiSrc</i>.


### -param dxSrc

Width of the source rectangle.


### -param dySrc

Height of the source rectangle.


### -param lpbiDst

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the output format. If the value of this parameter is <b>NULL</b>, the function determines whether the input format is supported and this parameter is ignored.


### -param lpDst


            Pointer to a buffer that is large enough to contain the decompressed data.
          


### -param xDst


            The x-coordinate of the destination rectangle for the DIB specified by <i>lpbiDst</i>.
          


### -param yDst


            The y-coordinate of the destination rectangle for the DIB specified by <i>lpbiDst</i>.
          


### -param dxDst


            Width of the destination rectangle.
          


### -param dyDst


            Height of the destination rectangle.
          


## -returns




            Returns <b>ICERR_OK</b> if successful or an error otherwise.
          




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

