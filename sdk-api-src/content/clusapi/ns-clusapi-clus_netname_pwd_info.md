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

# CLUS_NETNAME_PWD_INFO structure


## -description


Provides information for resetting the security principal associated with a computer name.


## -struct-fields




### -field Flags

Indicates if other fields in the structure have valid data.


### -field Password

Contains the new password for the alternate computer name's associated security principal.


### -field CreatingDC

Contains the name of a directory server where the associated security principal object is stored. The total length includes the '\\' prefix.


### -field ObjectGuid

Contains the ID of a security principal objecton a directory server.


## -see-also




<a href="https://msdn.microsoft.com/640359e9-ed65-46c1-a9d4-655e2f6a24df">Failover Cluster Structures</a>
 

 

