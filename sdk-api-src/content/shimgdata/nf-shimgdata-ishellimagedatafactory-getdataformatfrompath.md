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

# IShellImageDataFactory::GetDataFormatFromPath


## -description


Determines a file's format based on its extension.


## -parameters




### -param pszPath [in]

Type: <b>LPCWSTR</b>

A path to the file.


### -param pDataFormat [out]

Type: <b>GUID*</b>

A pointer to a GUID identifying the image format of the file.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

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
The <i>pszPath</i> parameter is <b>NULL</b>, the file name extension does not correspond to any defined GDI+ decoder, or an internal error has occurred. In any of these cases, <i>pDataFormat</i> is set to GUID_NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The internal object cannot be instantiated.

</td>
</tr>
</table>
 




## -remarks



<b>IShellImageDataFactory::GetDataFormatFromPath</b> should only be used to determine whether data can be saved to a particular format on the current system.



