---
UID: NS:clusapi._CLUS_CHKDSK_INFO
title: CLUS_CHKDSK_INFO (clusapi.h)
description: Represents information about a Chkdsk operation.
helpviewer_keywords: ["*PCLUS_CHKDSK_INFO","CLUS_CHKDSK_INFO","CLUS_CHKDSK_INFO structure [Failover Cluster]","PCLUS_CHKDSK_INFO","PCLUS_CHKDSK_INFO structure pointer [Failover Cluster]","clusapi/CLUS_CHKDSK_INFO","clusapi/PCLUS_CHKDSK_INFO","mscs.clus_chkdsk_info"]
old-location: mscs\clus_chkdsk_info.htm
tech.root: MsCS
ms.assetid: 455DD59C-B54D-4B42-B661-2E3994E69718
ms.date: 12/05/2018
ms.keywords: '*PCLUS_CHKDSK_INFO, CLUS_CHKDSK_INFO, CLUS_CHKDSK_INFO structure [Failover Cluster], PCLUS_CHKDSK_INFO, PCLUS_CHKDSK_INFO structure pointer [Failover Cluster], clusapi/CLUS_CHKDSK_INFO, clusapi/PCLUS_CHKDSK_INFO, mscs.clus_chkdsk_info'
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
req.typenames: CLUS_CHKDSK_INFO, *PCLUS_CHKDSK_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUS_CHKDSK_INFO
 - clusapi/_CLUS_CHKDSK_INFO
 - PCLUS_CHKDSK_INFO
 - clusapi/PCLUS_CHKDSK_INFO
 - CLUS_CHKDSK_INFO
 - clusapi/CLUS_CHKDSK_INFO
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
 - CLUS_CHKDSK_INFO
---

# CLUS_CHKDSK_INFO structure


## -description

Represents information about a Chkdsk operation.

## -struct-fields

### -field PartitionNumber

The ID of the partition on which the Chkdsk operation is being performed.

### -field ChkdskState

The state of the Chkdsk operation.

### -field FileIdCount

The number of files that were identified by the Chkdsk operation.

### -field FileIdList

A list of file IDs that were identified by the Chkdsk operation.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>