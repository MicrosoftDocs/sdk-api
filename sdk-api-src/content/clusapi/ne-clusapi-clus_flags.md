---
UID: NE:clusapi.CLUS_FLAGS
title: CLUS_FLAGS
author: windows-sdk-content
description: Identifies the resource or group as a core resource.
old-location: mscs\clus_flags.htm
tech.root: MsCS
ms.assetid: 54d00b1c-cef7-4310-8c10-743ee7086979
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CLUS_FLAGS, CLUS_FLAGS enumeration [Failover Cluster], CLUS_FLAG_CORE, _CLUS_FLAGS, _CLUS_FLAGS enumeration [Failover Cluster], clusapi/CLUS_FLAGS, clusapi/CLUS_FLAG_CORE, clusapi/_CLUS_FLAGS, msclus/CLUS_FLAGS, msclus/CLUS_FLAG_CORE, msclus/_CLUS_FLAGS, mscs.clus_flags
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUS_FLAGS
product: Windows
targetos: Windows
req.typenames: CLUS_FLAGS
req.redist: 
---

# CLUS_FLAGS enumeration


## -description


Identifies the resource or group as a 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369314(v=VS.85).aspx">core resource</a>.


## -enum-fields




### -field CLUS_FLAG_CORE

Identifies <a href="https://msdn.microsoft.com/en-us/library/Aa369314(v=VS.85).aspx">core resources</a> or the cluster group that 
       contains core resources. The 
       <a href="https://msdn.microsoft.com/en-us/library/Aa369016(v=VS.85).aspx">ClusterResourceControl</a> function with the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa367471(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_FLAGS</a> control 
       code can retrieve the flags that are set for a resource.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa367471(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_FLAGS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369016(v=VS.85).aspx">ClusterResourceControl</a>
 

 

