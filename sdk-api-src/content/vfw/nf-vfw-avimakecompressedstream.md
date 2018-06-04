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

# AVIMakeCompressedStream function


## -description



The <b>AVIMakeCompressedStream</b> function creates a compressed stream from an uncompressed stream and a compression filter, and returns the address of a pointer to the compressed stream. This function supports audio and video compression.




## -parameters




### -param ppsCompressed

Pointer to a buffer that receives the compressed stream pointer.


### -param ppsSource

TBD


### -param lpOptions

Pointer to a structure that identifies the type of compression to use and the options to apply. You can specify video compression by identifying an appropriate handler in the <a href="https://msdn.microsoft.com/8084adc3-792f-4a6c-b407-51e0e435e629">AVICOMPRESSOPTIONS</a> structure. For audio compression, specify the compressed data format.


### -param pclsidHandler

Pointer to a class identifier used to create the stream.


#### - psSource

Pointer to the stream to be compressed.


## -returns



Returns AVIERR_OK if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_NOCOMPRESSOR</b></dt>
</dl>
</td>
<td width="60%">
A suitable compressor cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AVIERR_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Compression is not supported for this type of data. This error might be returned if you try to compress data that is not audio or video.

</td>
</tr>
</table>
 




## -remarks



Applications can read from or write to the compressed stream.

A <b>PAVISTREAM</b> is a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

