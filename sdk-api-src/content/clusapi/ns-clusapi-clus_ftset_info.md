---
UID: NS:clusapi.CLUS_FTSET_INFO
title: CLUS_FTSET_INFO (clusapi.h)
description: Contains information about an FT (fault tolerant) set. This structure is used by the CLUSPROP_FTSET_INFO structure to create an entry in a value list.
helpviewer_keywords: ["*PCLUS_FTSET_INFO","CLUS_FTSET_INFO","CLUS_FTSET_INFO structure [Failover Cluster]","PCLUS_FTSET_INFO","PCLUS_FTSET_INFO structure pointer [Failover Cluster]","clusapi/CLUS_FTSET_INFO","clusapi/PCLUS_FTSET_INFO","mscs.clus_ftset_info"]
old-location: mscs\clus_ftset_info.htm
tech.root: MsCS
ms.assetid: 75F2589D-8F4F-4B65-AE05-DA48A1EED03F
ms.date: 12/05/2018
ms.keywords: '*PCLUS_FTSET_INFO, CLUS_FTSET_INFO, CLUS_FTSET_INFO structure [Failover Cluster], PCLUS_FTSET_INFO, PCLUS_FTSET_INFO structure pointer [Failover Cluster], clusapi/CLUS_FTSET_INFO, clusapi/PCLUS_FTSET_INFO, mscs.clus_ftset_info'
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
req.typenames: CLUS_FTSET_INFO, *PCLUS_FTSET_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_FTSET_INFO
 - clusapi/CLUS_FTSET_INFO
 - PCLUS_FTSET_INFO
 - clusapi/PCLUS_FTSET_INFO
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
 - CLUS_FTSET_INFO
---

# CLUS_FTSET_INFO structure


## -description

Contains information about an FT (fault tolerant) set. This structure is used by the <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_ftset_info">CLUSPROP_FTSET_INFO</a> structure to create an entry in a value list.

## -struct-fields

### -field dwRootSignature

The root signature of the FT set.

### -field dwFtType

The type of fault tolerance that is supported by the FT set.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_ftset_info">CLUSPROP_FTSET_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>