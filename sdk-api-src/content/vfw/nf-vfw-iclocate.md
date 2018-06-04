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

# ICLocate function


## -description



The <b>ICLocate</b> function finds a compressor or decompressor that can handle images with the specified formats, or finds a driver that can decompress an image with a specified format directly to hardware.




## -parameters




### -param fccType


            Four-character code indicating the type of compressor or decompressor to open. For video streams, the value of this parameter is 'VIDC'.
          


### -param fccHandler


            Preferred handler of the specified type. Typically, the handler type is stored in the stream header in an AVI file. Specify <b>NULL</b> if your application can use any handler type or it does not know the handler type to use.
          


### -param lpbiIn


            Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure defining the input format. A compressor handle is not returned unless it supports this format.
          


### -param lpbiOut

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure defining an optional decompressed format. You can also specify zero to use the default output format associated with the input format.

If this parameter is nonzero, a compressor handle is not returned unless it can create this output format.


### -param wFlags


            Flags that describe the search criteria for a compressor or decompressor. The following values are defined:
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICMODE_COMPRESS"></a><a id="icmode_compress"></a><dl>
<dt><b>ICMODE_COMPRESS</b></dt>
</dl>
</td>
<td width="60%">
Finds a compressor that can compress an image with a format defined by <i>lpbiIn</i> to the format defined by <i>lpbiOut</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="ICMODE_DECOMPRESS"></a><a id="icmode_decompress"></a><dl>
<dt><b>ICMODE_DECOMPRESS</b></dt>
</dl>
</td>
<td width="60%">

            Finds a decompressor that can decompress an image with a format defined by <i>lpbiIn</i> to the format defined by <i>lpbiOut</i>.
          

</td>
</tr>
<tr>
<td width="40%"><a id="ICMODE_DRAW"></a><a id="icmode_draw"></a><dl>
<dt><b>ICMODE_DRAW</b></dt>
</dl>
</td>
<td width="60%">

            Finds a decompressor that can decompress an image with a format defined by <i>lpbiIn</i> and draw it directly to hardware.
          

</td>
</tr>
<tr>
<td width="40%"><a id="ICMODE_FASTCOMPRESS"></a><a id="icmode_fastcompress"></a><dl>
<dt><b>ICMODE_FASTCOMPRESS</b></dt>
</dl>
</td>
<td width="60%">

            Has the same meaning as <b>ICMODE_COMPRESS</b> except the compressor is used for a real-time operation and emphasizes speed over quality.
          

</td>
</tr>
<tr>
<td width="40%"><a id="ICMODE_FASTDECOMPRESS"></a><a id="icmode_fastdecompress"></a><dl>
<dt><b>ICMODE_FASTDECOMPRESS</b></dt>
</dl>
</td>
<td width="60%">

            Has the same meaning as <b>ICMODE_DECOMPRESS</b> except the decompressor is used for a real-time operation and emphasizes speed over quality.
          

</td>
</tr>
</table>
 


## -returns



Returns a handle to a compressor or decompressor if successful or zero otherwise.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

