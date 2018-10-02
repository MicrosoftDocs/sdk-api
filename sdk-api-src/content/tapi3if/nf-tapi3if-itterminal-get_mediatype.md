---
UID: NF:tapi3if.ITTerminal.get_MediaType
title: ITTerminal::get_MediaType
author: windows-sdk-content
description: The get_MediaType method determines the media that this terminal supports.
old-location: tapi3\itterminal_get_mediatype.htm
tech.root: TAPI
ms.assetid: 8c2006ad-d2f9-4e21-b0ae-583ec3ff82f4
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITTerminal interface [TAPI 2.2],get_MediaType method, ITTerminal.get_MediaType, ITTerminal::get_MediaType, _tapi3_itterminal_get_mediatype, get_MediaType, get_MediaType method [TAPI 2.2], get_MediaType method [TAPI 2.2],ITTerminal interface, tapi3.itterminal_get_mediatype, tapi3if/ITTerminal::get_MediaType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminal.get_MediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminal::get_MediaType


## -description


The 
<b>get_MediaType</b> method determines the media that this terminal supports.


## -parameters




### -param plMediaType [out]

Pointer to 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plMediaType</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>
 

 

