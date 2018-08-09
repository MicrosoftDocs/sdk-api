---
UID: NE:clusapi.CLUS_RESSUBCLASS
title: CLUS_RESSUBCLASS
author: windows-sdk-content
description: Identifies a resource subclass that manages a shared resource.
old-location: mscs\clus_ressubclass.htm
old-project: mscs
ms.assetid: 2e10a529-a12d-4259-a18a-be96471ab3a5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CLUS_RESSUBCLASS, CLUS_RESSUBCLASS enumeration [Failover Cluster], CLUS_RESSUBCLASS_SHARED, _CLUS_RESSUBCLASS, _CLUS_RESSUBCLASS enumeration [Failover Cluster], clusapi/CLUS_RESSUBCLASS, clusapi/CLUS_RESSUBCLASS_SHARED, clusapi/_CLUS_RESSUBCLASS, msclus/CLUS_RESSUBCLASS, msclus/CLUS_RESSUBCLASS_SHARED, msclus/_CLUS_RESSUBCLASS, mscs.clus_ressubclass
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: clusapi.h
req.include-header: 
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
req.typenames: CLUS_RESSUBCLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUS_RESSUBCLASS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CLUS_RESSUBCLASS enumeration


## -description


Identifies a resource subclass that manages a shared resource.


## -enum-fields




### -field CLUS_RESSUBCLASS_SHARED

Identifies a resource subclass that manages a shared resource, such as a disk on a shared SCSI bus. The 
      <a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a> function with the 
      <a href="https://msdn.microsoft.com/4c4f8809-d6eb-43e1-a09e-cfe3770a1fd4">CLUSCTL_RESOURCE_GET_CLASS_INFO</a> 
      control code can retrieve a 
      <a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a> structure that contains 
      this information.


## -see-also




<a href="https://msdn.microsoft.com/4c4f8809-d6eb-43e1-a09e-cfe3770a1fd4">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/b8b6c479-2e35-4cc9-b864-d495c3bded25">CLUS_RESOURCE_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/a98ca55a-6535-48cf-a925-5005baa01b94">ClusterResourceControl</a>
 

 

