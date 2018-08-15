---
UID: NE:clusapi.CLUS_RESSUBCLASS_STORAGE
title: CLUS_RESSUBCLASS_STORAGE
author: windows-sdk-content
description: Identifies a resource subclass that manages a shared bus.
old-location: mscs\clus_ressubclass_storage.htm
old-project: mscs
ms.assetid: 10e2fe05-ea17-4f9d-a26d-eed6aa3abb04
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CLUS_RESSUBCLASS_STORAGE, CLUS_RESSUBCLASS_STORAGE enumeration [Failover Cluster], CLUS_RESSUBCLASS_STORAGE_DISK, CLUS_RESSUBCLASS_STORAGE_REPLICATION, CLUS_RESSUBCLASS_STORAGE_SHARED_BUS, clusapi/CLUS_RESSUBCLASS_STORAGE, clusapi/CLUS_RESSUBCLASS_STORAGE_DISK, clusapi/CLUS_RESSUBCLASS_STORAGE_REPLICATION, clusapi/CLUS_RESSUBCLASS_STORAGE_SHARED_BUS, msclus/CLUS_RESSUBCLASS_STORAGE, msclus/CLUS_RESSUBCLASS_STORAGE_DISK, msclus/CLUS_RESSUBCLASS_STORAGE_REPLICATION, msclus/CLUS_RESSUBCLASS_STORAGE_SHARED_BUS, mscs.clus_ressubclass_storage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: clusapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CLUS_RESSUBCLASS_STORAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUS_RESSUBCLASS_STORAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CLUS_RESSUBCLASS_STORAGE enumeration


## -description


Identifies a resource subclass that manages a shared bus.


## -enum-fields




### -field CLUS_RESSUBCLASS_STORAGE_SHARED_BUS

Identifies a resource subclass that manages a shared bus. The 
      <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> function with the 
      <a href="https://msdn.microsoft.com/4c4f8809-d6eb-43e1-a09e-cfe3770a1fd4">CLUSCTL_RESOURCE_GET_CLASS_INFO</a> 
      control code can retrieve a 
      <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> structure that contains 
      information for a resource subclass.


### -field CLUS_RESSUBCLASS_STORAGE_DISK

Identifies a resource subclass that manages a disk.

<b>Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not supported before Windows Server 2012 R2.


### -field CLUS_RESSUBCLASS_STORAGE_REPLICATION

Identifies a resource subclass that manages storage replication.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not supported before Windows Server 2016.


## -see-also




<a href="https://msdn.microsoft.com/4c4f8809-d6eb-43e1-a09e-cfe3770a1fd4">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a>
 

 

