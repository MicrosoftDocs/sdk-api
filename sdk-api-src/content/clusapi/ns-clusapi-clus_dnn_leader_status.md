---
UID: NS:clusapi.CLUS_DNN_LEADER_STATUS
title: CLUS_DNN_LEADER_STATUS (clusapi.h)
description: Represents the status of a Distributed Network Name (DNN) resource for a Scale-Out File Server.
helpviewer_keywords: ["*PCLUS_DNN_LEADER_STATUS","CLUS_DNN_LEADER_STATUS","CLUS_DNN_LEADER_STATUS structure [Failover Cluster]","PCLUS_DNN_LEADER_STATUS","PCLUS_DNN_LEADER_STATUS structure pointer [Failover Cluster]","clusapi/CLUS_DNN_LEADER_STATUS","clusapi/PCLUS_DNN_LEADER_STATUS","mscs.clus_dnn_leader_status"]
old-location: mscs\clus_dnn_leader_status.htm
tech.root: MsCS
ms.assetid: 141629A8-95B3-409C-8165-D3AF055C41EB
ms.date: 12/05/2018
ms.keywords: '*PCLUS_DNN_LEADER_STATUS, CLUS_DNN_LEADER_STATUS, CLUS_DNN_LEADER_STATUS structure [Failover Cluster], PCLUS_DNN_LEADER_STATUS, PCLUS_DNN_LEADER_STATUS structure pointer [Failover Cluster], clusapi/CLUS_DNN_LEADER_STATUS, clusapi/PCLUS_DNN_LEADER_STATUS, mscs.clus_dnn_leader_status'
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
targetos: Windows
req.typenames: CLUS_DNN_LEADER_STATUS, *PCLUS_DNN_LEADER_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_DNN_LEADER_STATUS
 - clusapi/CLUS_DNN_LEADER_STATUS
 - PCLUS_DNN_LEADER_STATUS
 - clusapi/PCLUS_DNN_LEADER_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_DNN_LEADER_STATUS
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

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_dnn_sodafs_clone_status">CLUS_DNN_SODAFS_CLONE_STATUS</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>