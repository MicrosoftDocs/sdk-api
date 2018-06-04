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

# _PNRP_CLOUD_ID structure


## -description


The <b>PNRP_CLOUD_ID</b> structure contains the values that define a network cloud.


## -struct-fields




### -field AddressFamily

Must be AF_INET6.


### -field Scope

Specifies the scope of the cloud. Use one of the following values:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>PNRP_SCOPE_ANY</td>
<td>The cloud can be in any scope.</td>
</tr>
<tr>
<td>PNRP_GLOBAL_SCOPE</td>
<td>The cloud must be a global scope.</td>
</tr>
<tr>
<td>PNRP_SITE_LOCAL_SCOPE</td>
<td>The cloud must be a site-local scope.</td>
</tr>
<tr>
<td>PNRP_LINK_LOCAL_SCOPE</td>
<td>The cloud must be a link-local scope.</td>
</tr>
</table>
 


### -field ScopeId

Specifies the ID for this scope.


## -see-also




<a href="https://msdn.microsoft.com/82af5a4f-1b29-405a-a200-1d723ea7693b">PNRPCLOUDINFO</a>
 

 

