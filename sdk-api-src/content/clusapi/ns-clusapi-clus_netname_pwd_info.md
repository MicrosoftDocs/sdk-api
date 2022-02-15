---
UID: NS:clusapi.CLUS_NETNAME_PWD_INFO
title: CLUS_NETNAME_PWD_INFO (clusapi.h)
description: Provides information for resetting the security principal associated with a computer name.
helpviewer_keywords: ["*PCLUS_NETNAME_PWD_INFO","*PCLUS_RLUA_PWD_INFO","CLUS_NETNAME_PWD_INFO","CLUS_NETNAME_PWD_INFO structure [Failover Cluster]","CLUS_RLUA_PWD_INFO","CLUS_RLUA_PWD_INFO structure [Failover Cluster]","PCLUS_NETNAME_PWD_INFO","PCLUS_NETNAME_PWD_INFO structure pointer [Failover Cluster]","PCLUS_RLUA_PWD_INFO","PCLUS_RLUA_PWD_INFO structure pointer [Failover Cluster]","clusapi/CLUS_NETNAME_PWD_INFO","clusapi/CLUS_RLUA_PWD_INFO","clusapi/PCLUS_NETNAME_PWD_INFO","clusapi/PCLUS_RLUA_PWD_INFO","mscs.clus_netname_pwd_info"]
old-location: mscs\clus_netname_pwd_info.htm
tech.root: MsCS
ms.assetid: 365959c8-63e7-477b-b772-85a0afdaa6f6
ms.date: 12/05/2018
ms.keywords: '*PCLUS_NETNAME_PWD_INFO, *PCLUS_RLUA_PWD_INFO, CLUS_NETNAME_PWD_INFO, CLUS_NETNAME_PWD_INFO structure [Failover Cluster], CLUS_RLUA_PWD_INFO, CLUS_RLUA_PWD_INFO structure [Failover Cluster], PCLUS_NETNAME_PWD_INFO, PCLUS_NETNAME_PWD_INFO structure pointer [Failover Cluster], PCLUS_RLUA_PWD_INFO, PCLUS_RLUA_PWD_INFO structure pointer [Failover Cluster], clusapi/CLUS_NETNAME_PWD_INFO, clusapi/CLUS_RLUA_PWD_INFO, clusapi/PCLUS_NETNAME_PWD_INFO, clusapi/PCLUS_RLUA_PWD_INFO, mscs.clus_netname_pwd_info'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
req.typenames: CLUS_NETNAME_PWD_INFO, *PCLUS_NETNAME_PWD_INFO, CLUS_RLUA_PWD_INFO, *PCLUS_RLUA_PWD_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_NETNAME_PWD_INFO
 - clusapi/CLUS_NETNAME_PWD_INFO
 - PCLUS_NETNAME_PWD_INFO
 - clusapi/PCLUS_NETNAME_PWD_INFO
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
 - CLUS_NETNAME_PWD_INFO
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

Contains the ID of a security principal object on a directory server.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-structures">Failover Cluster Structures</a>