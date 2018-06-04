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

# ICatInformation::GetCategoryDesc


## -description


Retrieves the localized description string for a specific category ID.


## -parameters




### -param rcatid [in]

The category identifier.


### -param lcid [in]

The locale.


### -param pszDesc [out]

A pointer to the string pointer for the description. This string must be released by the caller using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CAT_E_CATIDNOEXIST</b></dt>
</dl>
</td>
<td width="60%">
The category ID <i>rcatid</i> is not registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CAT_E_NODESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
There is no description string for <i>rcatid</i> with the specified locale.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1fd68126-b512-4131-8e93-cea7c1c3e9c0">ICatInformation</a>
 

 

