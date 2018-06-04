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

# IShellImageData::GetEncoderParams


## -description


Gets the current set of encoder parameters.


## -parameters




### -param pguidFmt [in]

Type: <b>GUID*</b>

A pointer to a GUID that specifies the encoder. This must be an encoder supported by GDI+. If this parameter is <b>NULL</b>, an unhandled exception results.


### -param ppEncParams [out]

Type: <b>EncoderParameters**</b>

The address of a pointer to an array of <a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a> objects.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Several circumstances can generate this return value.
                        

<ul>
<li>The image was not decoded or the decoding process failed.</li>
<li><i>pguidFmt</i> refers to a format not supported by GDI+.</li>
<li>An internal call failed.</li>
</ul>
</td>
</tr>
</table>
 



