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

# _SR_RESOURCE_TYPE_QUERY_ELIGIBLE_LOGDISKS structure


## -description


Describes a set of retrieved disks that can be used as log disks for the specified data disk.
   This is a data structure for a value list that is returned by the <a href="https://msdn.microsoft.com/C0D7B513-27F5-4BAC-81E2-6B8290DBAAB9">CLUSCTL_RESOURCE_TYPE_REPLICATION_GET_ELIGIBLE_LOGDISKS</a> control code.


## -struct-fields




### -field DataDiskGuid

The cluster resource identifier of the data disk.


### -field IncludeOfflineDisks

When <b>TRUE</b>, the result set includes all the offline disks in the available storage group.


## -see-also




<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

