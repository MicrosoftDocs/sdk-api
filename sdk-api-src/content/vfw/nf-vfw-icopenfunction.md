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

# ICOpenFunction function


## -description



The <b>ICOpenFunction</b> function opens a compressor or decompressor defined as a function.




## -parameters




### -param fccType

Type of compressor to open. For video, the value of this parameter is ICTYPE_VIDEO.


### -param fccHandler

Preferred handler of the specified type. Typically, this comes from the stream header in an AVI file.


### -param wMode

Flag to define the use of the compressor or decompressor. The following values are defined.

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
<td>ICMODE_COMPRESS</td>
<td>Compressor will perform normal compression.</td>
</tr>
<tr>
<td>ICMODE_DECOMPRESS</td>
<td>Decompressor will perform normal decompression.</td>
</tr>
<tr>
<td>ICMODE_DRAW</td>
<td>Decompressor will decompress and draw the data directly to hardware.</td>
</tr>
<tr>
<td>ICMODE_FASTCOMPRESS</td>
<td>Compressor will perform fast (real-time) compression.</td>
</tr>
<tr>
<td>ICMODE_FASTDECOMPRESS</td>
<td>Decompressor will perform fast (real-time) decompression.</td>
</tr>
<tr>
<td>ICMODE_QUERY</td>
<td>Queries the compressor or decompressor for information.</td>
</tr>
</table>
 


### -param lpfnHandler

Pointer to the function used as the compressor or decompressor.


## -returns



Returns a handle to a compressor or decompressor if successful or zero otherwise.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

