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

# ISettingsEngine::GetNamespace


## -description


Opens an existing namespace as specified by the <a href="https://msdn.microsoft.com/aa9d5604-5b94-47d9-9e68-d708a656a5ea">ISettingsIdentity</a> parameter.


## -parameters




### -param SettingsID [in]

An <a href="https://msdn.microsoft.com/aa9d5604-5b94-47d9-9e68-d708a656a5ea">ISettingsIdentity</a> object that specifies an existing namespace to get.


### -param Access [in]

A <a href="https://msdn.microsoft.com/11918eab-2f5d-4050-81c6-d4c465b68ce3">WcmNamespaceAccess</a> value that specifies the type of access, whether it is read-only or read and write access.


### -param Reserved [in]

Reserved. Must be <b>NULL</b>.


### -param NamespaceItem [out]

A pointer to an <a href="https://msdn.microsoft.com/a5d7b9ff-eb6f-40be-b246-17189cad92be">ISettingsNamespace</a> object that is the result of the get operation.


## -returns



This method can return one of these values.

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
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_USERNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the store is not currently loaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_NAMESPACENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the provided identity does not match a namespace registered in the store.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ba816a00-e238-4dbd-a09a-ad4e191d9c4e">ISettingsEngine</a>
 

 

