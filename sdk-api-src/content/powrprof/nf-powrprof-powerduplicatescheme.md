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

# PowerDuplicateScheme function


## -description


Duplicates an existing power scheme.


## -parameters




### -param RootPowerKey [in, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.


### -param SourceSchemeGuid [in]

The identifier of the power scheme that is to be duplicated.


### -param DestinationSchemeGuid [in]

The address of a pointer to a <b>GUID</b>. If the pointer contains 
      <b>NULL</b>, the function allocates memory for a new 
      <b>GUID</b> and puts the address of this memory in the pointer. The caller can free this 
      memory using <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>.


## -returns



Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_SUCCESS</b></b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The power scheme was successfully duplicated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_INVALID_PARAMETER</b></b></dt>
<dt>87 (0x57)</dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>ERROR_ALREADY_EXISTS</b></b></dt>
<dt>183 (0xB7)</dt>
</dl>
</td>
<td width="60%">
The <i>DestinationSchemeGuid</i> parameter refers to an existing power scheme. 
        <a href="https://msdn.microsoft.com/5f9969a1-e598-4ca8-a5b8-f8bb3410223d">PowerDeleteScheme</a> can be used to delete this 
        scheme.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/eae96a9e-ced2-4e13-b250-33c5acbbae48">Power Management Functions</a>
 

 

