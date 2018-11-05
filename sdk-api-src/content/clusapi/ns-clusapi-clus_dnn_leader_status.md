---
UID: NS:clusapi.CLUS_DNN_LEADER_STATUS
title: CLUS_DNN_LEADER_STATUS
author: windows-sdk-content
description: Represents the status of a Distributed Network Name (DNN) resource for a Scale-Out File Server.
old-location: mscs\clus_dnn_leader_status.htm
tech.root: mscs
ms.assetid: 141629A8-95B3-409C-8165-D3AF055C41EB
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PCLUS_DNN_LEADER_STATUS, CLUS_DNN_LEADER_STATUS, CLUS_DNN_LEADER_STATUS structure [Failover Cluster], PCLUS_DNN_LEADER_STATUS, PCLUS_DNN_LEADER_STATUS structure pointer [Failover Cluster], clusapi/CLUS_DNN_LEADER_STATUS, clusapi/PCLUS_DNN_LEADER_STATUS, mscs.clus_dnn_leader_status"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
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
api_name:
 - CLUS_DNN_LEADER_STATUS
product: Windows
targetos: Windows
req.typenames: CLUS_DNN_LEADER_STATUS, *PCLUS_DNN_LEADER_STATUS
req.redist: 
---

# CLUS_DNN_LEADER_STATUS structure


## -description


Represents the status of a Distributed Network Name (DNN) resource for a Scale-Out File Server.


## -struct-fields




### -field IsOnline

<b>TRUE</b> if the Distributed Network Name (DNN) resource for the Scale-Out File Server  is online; otherwise <b>FALSE</b>.


### -field IsFileServerPresent

<b>TRUE</b> if the file server is running; otherwise <b>FALSE</b>.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn622926(v=VS.85).aspx">CLUS_DNN_SODAFS_CLONE_STATUS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369339(v=VS.85).aspx">Data structures</a>
 

 

