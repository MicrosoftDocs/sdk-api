---
UID: NF:dmort.MoCreateMediaType
title: MoCreateMediaType function
author: windows-sdk-content
description: The MoCreateMediaType function allocates a new media type structure.
old-location: dshow\mocreatemediatype.htm
tech.root: DirectShow
ms.assetid: f67b04b5-163e-4793-8df0-10a4b2be5025
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MoCreateMediaType, MoCreateMediaType function [DirectShow], dmort/MoCreateMediaType, dshow.mocreatemediatype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dmort.h
req.include-header: Dmo.h
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
req.lib: Msdmo.lib
req.dll: Msdmo.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdmo.dll
api_name:
 - MoCreateMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MoCreateMediaType
: 
---

# MoCreateMediaType function


## -description


The <b>MoCreateMediaType</b> function allocates a new media type structure.


## -parameters




### -param ppmt

Receives a pointer to an allocated <a href="https://msdn.microsoft.com/c545ddf7-9797-45ab-a42a-d8550b598e98">DMO_MEDIA_TYPE</a> structure.


### -param cbFormat

Number of bytes to allocate for the format block. Can be zero.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



This function allocates a new <a href="https://msdn.microsoft.com/c545ddf7-9797-45ab-a42a-d8550b598e98">DMO_MEDIA_TYPE</a> structure on the heap. It also allocates memory for the format block. The caller must delete the structure by calling the <a href="https://msdn.microsoft.com/adbfe1e1-e956-48de-9ed1-9f8f4c66ff1c">MoDeleteMediaType</a> function.

Internally, this function calls <a href="https://msdn.microsoft.com/526ad3c6-a002-4b79-9712-47ea9ce321ba">MoInitMediaType</a> to allocate the format block.





