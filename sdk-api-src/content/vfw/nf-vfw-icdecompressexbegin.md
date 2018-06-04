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

# ICDecompressExBegin function


## -description



The <b>ICDecompressExBegin</b> function prepares a decompressor for decompressing data.




## -parameters




### -param hic


            Handle to the decompressor to use.
          


### -param dwFlags


            Decompression flags. The following values are defined.
            

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Meaning
                </th>
</tr>
<tr>
<td><b>ICDECOMPRESS_HURRYUP</b></td>
<td>Tries to decompress at a faster rate. When an application uses this flag, the driver should buffer the decompressed data but not draw the image.</td>
</tr>
<tr>
<td><b>ICDECOMPRESS_NOTKEYFRAME</b></td>
<td>Current frame is not a key frame.</td>
</tr>
<tr>
<td><b>ICDECOMPRESS_NULLFRAME</b></td>
<td>Current frame does not contain data and the decompressed image should be left the same.</td>
</tr>
<tr>
<td><b>ICDECOMPRESS_PREROLL</b></td>
<td>Current frame precedes the point in the movie where playback starts and, therefore, will not be drawn.</td>
</tr>
<tr>
<td><b>ICDECOMPRESS_UPDATE</b></td>
<td>Screen is being updated or refreshed.</td>
</tr>
</table>
 


### -param lpbiSrc


            Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the format of the compressed data.
          


### -param lpSrc


            Pointer to the input data.
          


### -param xSrc


            The x-coordinate of the source rectangle for the DIB specified by <i>lpbiSrc</i>.
          


### -param ySrc


            The y-coordinate of the source rectangle for the DIB specified by <i>lpbiSrc</i>.
          


### -param dxSrc


            Width of the source rectangle.
          


### -param dySrc


            Height of the source rectangle.
          


### -param lpbiDst


            Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the output format.
          


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
 

 

