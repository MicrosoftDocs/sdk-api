---
UID: NS:clusapi.CLUS_NETNAME_VS_TOKEN_INFO
title: CLUS_NETNAME_VS_TOKEN_INFO (clusapi.h)
description: Contains the data needed to request a token. It is used as the input parameter of the CLUSCTL_RESOURCE_NETNAME_GET_VIRTUAL_SERVER_TOKEN control code.
helpviewer_keywords: ["*PCLUS_NETNAME_VS_TOKEN_INFO","*PCLUS_VS_TOKEN_INFO","CLUS_NETNAME_VS_TOKEN_INFO","CLUS_NETNAME_VS_TOKEN_INFO structure [Failover Cluster]","CLUS_VS_TOKEN_INFO","CLUS_VS_TOKEN_INFO structure [Failover Cluster]","PCLUS_NETNAME_VS_TOKEN_INFO","PCLUS_NETNAME_VS_TOKEN_INFO structure pointer [Failover Cluster]","PCLUS_VS_TOKEN_INFO","PCLUS_VS_TOKEN_INFO structure pointer [Failover Cluster]","clusapi/CLUS_NETNAME_VS_TOKEN_INFO","clusapi/CLUS_VS_TOKEN_INFO","clusapi/PCLUS_NETNAME_VS_TOKEN_INFO","clusapi/PCLUS_VS_TOKEN_INFO","mscs.clus_netname_vs_token_info"]
old-location: mscs\clus_netname_vs_token_info.htm
tech.root: MsCS
ms.assetid: 9b4fc589-f4e4-4fcf-b3df-3b0b6f9f4e65
ms.date: 12/05/2018
ms.keywords: '*PCLUS_NETNAME_VS_TOKEN_INFO, *PCLUS_VS_TOKEN_INFO, CLUS_NETNAME_VS_TOKEN_INFO, CLUS_NETNAME_VS_TOKEN_INFO structure [Failover Cluster], CLUS_VS_TOKEN_INFO, CLUS_VS_TOKEN_INFO structure [Failover Cluster], PCLUS_NETNAME_VS_TOKEN_INFO, PCLUS_NETNAME_VS_TOKEN_INFO structure pointer [Failover Cluster], PCLUS_VS_TOKEN_INFO, PCLUS_VS_TOKEN_INFO structure pointer [Failover Cluster], clusapi/CLUS_NETNAME_VS_TOKEN_INFO, clusapi/CLUS_VS_TOKEN_INFO, clusapi/PCLUS_NETNAME_VS_TOKEN_INFO, clusapi/PCLUS_VS_TOKEN_INFO, mscs.clus_netname_vs_token_info'
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
req.typenames: CLUS_NETNAME_VS_TOKEN_INFO, CLUS_VS_TOKEN_INFO, *PCLUS_NETNAME_VS_TOKEN_INFO, *PCLUS_VS_TOKEN_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_NETNAME_VS_TOKEN_INFO
 - clusapi/CLUS_NETNAME_VS_TOKEN_INFO
 - PCLUS_NETNAME_VS_TOKEN_INFO
 - clusapi/PCLUS_NETNAME_VS_TOKEN_INFO
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
 - CLUS_NETNAME_VS_TOKEN_INFO
---

# CLUS_NETNAME_VS_TOKEN_INFO structure


## -description

Contains the data needed to request a token. It is used as the input parameter of the <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-netname-get-virtual-server-token">CLUSCTL_RESOURCE_NETNAME_GET_VIRTUAL_SERVER_TOKEN</a> control code.

## -struct-fields

### -field ProcessID

Process ID of the process requesting the token.

### -field DesiredAccess

Specifies an access mask that specifies the requested types of access. For a list of access rights for access 
      tokens, see 
      <a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>.

### -field InheritHandle

Indicates whether the new handle is inheritable. If <b>TRUE</b>, the duplicate handle can 
      be inherited by new processes created by the target process. If <b>FALSE</b>, the new handle 
      cannot be inherited.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-netname-get-virtual-server-token">CLUSCTL_RESOURCE_NETNAME_GET_VIRTUAL_SERVER_TOKEN</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data Structures</a>