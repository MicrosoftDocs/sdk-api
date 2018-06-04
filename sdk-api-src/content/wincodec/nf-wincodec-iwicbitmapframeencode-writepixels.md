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

# IWICBitmapFrameEncode::WritePixels


## -description


Copies scan-line data from a caller-supplied buffer to the <a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a> object.



## -parameters




### -param lineCount [in]

Type: <b>UINT</b>

The number of lines to encode.


### -param cbStride [in]

Type: <b>UINT</b>

The <a href="https://docs.microsoft.com/">stride</a> of the image pixels.


### -param cbBufferSize [in]

Type: <b>UINT</b>

The size of the pixel buffer.


### -param pbPixels [in]

Type: <b>BYTE*</b>

A pointer to the pixel buffer.


## -returns



Type: <b>HRESULT</b>

Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINCODEC_ERR_CODECTOOMANYSCANLINES</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>lineCount</i> is larger than the number of scan lines in the image.

</td>
</tr>
</table>
 




## -remarks



Successive <b>WritePixels</b> calls are assumed to be sequential scan-line access in the output image.



