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

# DFS_NAMESPACE_VERSION_ORIGIN enumeration


## -description


Identifies the origin of DFS namespace version information.


## -enum-fields




### -field DFS_NAMESPACE_VERSION_ORIGIN_COMBINED

The version information specifies the maximum version that the server and the Active Directory Domain Service (AD DS) domain can support.


### -field DFS_NAMESPACE_VERSION_ORIGIN_SERVER

The version information specifies the maximum version that the server can support.


### -field DFS_NAMESPACE_VERSION_ORIGIN_DOMAIN

The version information specifies the maximum version that the AD DS domain can support.


## -see-also




<a href="https://msdn.microsoft.com/ee75c500-70c6-4dce-9d38-36cacd695746">DFS_SUPPORTED_NAMESPACE_VERSION_INFO</a>



<a href="https://msdn.microsoft.com/c4ce8f50-f090-4783-b6c9-834d9e0c33de">NetDfsAddRootTarget</a>



<a href="https://msdn.microsoft.com/32ccf4a7-9d07-45e1-93db-29eddee01680">NetDfsGetSupportedNamespaceVersion</a>
 

 

