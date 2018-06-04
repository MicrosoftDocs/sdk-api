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

# _DFS_SUPPORTED_NAMESPACE_VERSION_INFO structure


## -description


Contains version information for a DFS namespace.


## -struct-fields




### -field DomainDfsMajorVersion

The major version of the domain-based DFS namespace.


### -field DomainDfsMinorVersion

 


### -field DomainDfsCapabilities

Specifies a set of flags that describe specific capabilities of a domain-based DFS namespace.



#### DFS_NAMESPACE_CAPABILITY_ABDE (0x0000000000000001)

The DFS namespace supports associating a security descriptor with a DFS link for Access-Based Directory Enumeration (ABDE) purposes.


### -field StandaloneDfsMajorVersion

The major version of the stand-alone DFS namespace.


### -field StandaloneDfsMinorVersion

The minor version of the stand-alone DFS namespace.


### -field StandaloneDfsCapabilities

Specifies a set of flags that describe specific capabilities of a stand-alone DFS namespace.



#### DFS_NAMESPACE_CAPABILITY_ABDE (0x0000000000000001)

The DFS namespace supports associating a security descriptor with a DFS link for ABDE purposes.


#### - NamespaceMinorVersion

The minor version of the domain-based DFS namespace.


## -see-also




<a href="https://msdn.microsoft.com/b260e132-41fd-460b-87e6-c6e0490dc8b4">DFS_NAMESPACE_VERSION_ORIGIN</a>



<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System Functions</a>



<a href="https://msdn.microsoft.com/c4ce8f50-f090-4783-b6c9-834d9e0c33de">NetDfsAddRootTarget</a>



<a href="https://msdn.microsoft.com/32ccf4a7-9d07-45e1-93db-29eddee01680">NetDfsGetSupportedNamespaceVersion</a>
 

 

