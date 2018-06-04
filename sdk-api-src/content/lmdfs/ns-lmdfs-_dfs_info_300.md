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

# _DFS_INFO_300 structure


## -description


Contains the name and type (domain-based or stand-alone) of a DFS namespace.


## -struct-fields




### -field Flags

Value that specifies the type of the DFS namespace. This member can be one of the following values.



#### DFS_VOLUME_FLAVOR_STANDALONE (0x00000100)

Specifies a stand-alone DFS namespace.



#### DFS_VOLUME_FLAVOR_AD_BLOB (0x00000200)

Specifies a domain-based DFS namespace.


### -field DfsName

Pointer to a null-terminated Unicode string that contains the name of a DFS namespace. This member can have one of the following two formats.

The first format is:

\<i>ServerName</i>\<i>DfsName</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone DFS namespace and <i>DfsName</i> is the name of the DFS namespace.

The second format is:

\<i>DomainName</i>\<i>DomDfsName</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS namespace and <i>DomDfsname</i> is the name of the DFS namespace.


## -remarks



The DFS functions use the 
<b>DFS_INFO_300</b> structure to enumerate DFS namespaces hosted on a machine.




## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

