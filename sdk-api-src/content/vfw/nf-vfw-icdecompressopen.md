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

# ICDecompressOpen macro


## -description



The <b>ICDecompressOpen</b> macro opens a decompressor that is compatible with the specified formats.




## -parameters




### -param fccType

Four-character code indicating the type of compressor to open. For video streams, the value of this parameter is "VIDC" or ICTYPE_VIDEO. 


### -param fccHandler

Four-character code indicating the preferred stream handler to use. Typically, this information is stored in the stream header in an AVI file. 


### -param lpbiIn

Pointer to a structure defining the input format. A decompressor handle is not returned unless it can decompress this format. For bitmaps, this parameter refers to a BITMAPINFOHEADER structure. 


### -param lpbiOut

Pointer to a structure defining an optional decompression format. You can also specify zero to use the default output format associated with the input format. 

If this parameter is nonzero, a compressor handle is not returned unless it can create this output format. For bitmaps, this parameter refers to a BITMAPINFOHEADER structure.



## -remarks



The <b>ICDecompressOpen</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define ICDecompressOpen(fccType, fccHandler, lpbiIn, lpbiOut) \ 
    ICLocate(fccType, fccHandler, lpbiIn, lpbiOut, ICMODE_DECOMPRESS); 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

