---
UID: NS:clusapi.CLUS_NETNAME_VS_TOKEN_INFO
title: CLUS_NETNAME_VS_TOKEN_INFO (clusapi.h)
author: windows-sdk-content
description: Contains the data needed to request a token. It is used as the input parameter of the CLUSCTL_RESOURCE_NETNAME_GET_VIRTUAL_SERVER_TOKEN control code.
old-location: mscs\clus_netname_vs_token_info.htm
tech.root: MsCS
ms.assetid: 9b4fc589-f4e4-4fcf-b3df-3b0b6f9f4e65
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCLUS_NETNAME_VS_TOKEN_INFO, *PCLUS_VS_TOKEN_INFO, CLUS_NETNAME_VS_TOKEN_INFO, CLUS_NETNAME_VS_TOKEN_INFO structure [Failover Cluster], CLUS_VS_TOKEN_INFO, CLUS_VS_TOKEN_INFO structure [Failover Cluster], PCLUS_NETNAME_VS_TOKEN_INFO, PCLUS_NETNAME_VS_TOKEN_INFO structure pointer [Failover Cluster], PCLUS_VS_TOKEN_INFO, PCLUS_VS_TOKEN_INFO structure pointer [Failover Cluster], clusapi/CLUS_NETNAME_VS_TOKEN_INFO, clusapi/CLUS_VS_TOKEN_INFO, clusapi/PCLUS_NETNAME_VS_TOKEN_INFO, clusapi/PCLUS_VS_TOKEN_INFO, mscs.clus_netname_vs_token_info"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_NETNAME_VS_TOKEN_INFO
product: Windows
targetos: Windows
req.typenames: CLUS_NETNAME_VS_TOKEN_INFO, CLUS_VS_TOKEN_INFO, *PCLUS_NETNAME_VS_TOKEN_INFO, *PCLUS_VS_TOKEN_INFO
req.redist: 
---

# CLUS_NETNAME_VS_TOKEN_INFO structure


## -description


Contains the data needed to request a token. It is used as the input parameter of the <a href="https://msdn.microsoft.com/7a1033be-1b97-49d6-91f3-78f5efed1f4b">CLUSCTL_RESOURCE_NETNAME_GET_VIRTUAL_SERVER_TOKEN</a> control code.


## -struct-fields




### -field ProcessID

Process ID of the process requesting the token.


### -field DesiredAccess

Specifies an access mask that specifies the requested types of access. For a list of access rights for access 
      tokens, see 
      <a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>.


### -field InheritHandle

Indicates whether the new handle is inheritable. If <b>TRUE</b>, the duplicate handle can 
      be inherited by new processes created by the target process. If <b>FALSE</b>, the new handle 
      cannot be inherited.


## -see-also




<a href="https://msdn.microsoft.com/7a1033be-1b97-49d6-91f3-78f5efed1f4b">CLUSCTL_RESOURCE_NETNAME_GET_VIRTUAL_SERVER_TOKEN</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

