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

# TdhUnloadManifest function


## -description


Unloads the manifest that was loaded by the <a href="https://msdn.microsoft.com/85dfcf73-ea3a-47e2-ad1a-3891b3917ecf">TdhLoadManifest</a> function.


## -parameters




### -param Manifest [in]

The full path to the loaded manifest.


## -returns



Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The manifest file was not found at the specified path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Manifest</i> parameter cannot be <b>NULL</b> and the path cannot exceed MAX_PATH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_XML_PARSE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The manifest did not pass validation. To determine the validation errors, run the manifest through the message compiler (mc.exe).

</td>
</tr>
</table>
 




## -remarks



You must call this function after processing all the events. For example, you can call this function after calling <a href="https://msdn.microsoft.com/25f4c4d3-0b70-40fe-bf03-8f9ffd82fbec">CloseTrace</a>.




## -see-also




<a href="https://msdn.microsoft.com/85dfcf73-ea3a-47e2-ad1a-3891b3917ecf">TdhLoadManifest</a>
 

 

