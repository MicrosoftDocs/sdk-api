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

# IShellImageData::GetResolution


## -description


Gets the resolution, in dots per inch (dpi), of the image.


## -parameters




### -param puResolutionX [out]

Type: <b>ULONG*</b>

A pointer to the horizontal resolution.


### -param puResolutionY [out]

Type: <b>ULONG*</b>

A pointer to the vertical resolution.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful or an error value otherwise, including the following:

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
The image has not been decoded, the decode process failed, or the resolution cannot be retrieved. In the latter case, both <i>puResolutionX</i> and <i>puResolutionY</i> are set to 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Both <i>puResolutionX</i> and <i>puResolutionY</i> are <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



If either <i>puResolutionX</i> or <i>puResolutionY</i> are <b>NULL</b>, the method returns only the value for the non-null parameter.



