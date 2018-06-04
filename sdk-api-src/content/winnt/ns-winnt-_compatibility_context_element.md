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

# _COMPATIBILITY_CONTEXT_ELEMENT structure


## -description


The <b>COMPATIBILITY_CONTEXT_ELEMENT</b> structure is used by the <a href="https://msdn.microsoft.com/7d45f63f-0baf-4236-b245-d36f9eb32e8c">QueryActCtxW</a> function as part of the <a href="https://msdn.microsoft.com/d8c1ef4a-8e64-45bd-a185-b4af7932a0d2">ACTIVATION_CONTEXT_COMPATIBILITY_INFORMATION</a> structure.



## -struct-fields




### -field Id

This is a <b>GUID</b> that specifies a version of  Windows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>{e2011457-1546-43c5-a5fe-008deee3d3f0}</dt>
</dl>
</td>
<td width="60%">
Windows Vista

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</dt>
</dl>
</td>
<td width="60%">
Windows 7

</td>
</tr>
</table>
 


### -field Type

A value of the <a href="https://msdn.microsoft.com/3a3c99e5-9a73-4688-8192-baee0078c17c">ACTCTX_COMPATIBILITY_ELEMENT_TYPE</a> enumeration that describes the compatibility elements in the application manifest.

