---
UID: NF:clusapi.GetCurrentClusterNodeId
title: GetCurrentClusterNodeId macro (clusapi.h)

description: Returns the unique identifier of the current cluster node.
old-location: mscs\getcurrentclusternodeid.htm
tech.root: MsCS
ms.assetid: 289abaaa-d063-4e99-91e7-441c58f7f75c

ms.date: 12/05/2018
ms.keywords: GetCurrentClusterNodeId, GetCurrentClusterNodeId macro [Failover Cluster], clusapi/GetCurrentClusterNodeId, mscs.getcurrentclusternodeid
ms.topic: macro
f1_keywords: 
 - "clusapi/GetCurrentClusterNodeId"
dev_langs:
 - c++
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
api_name:
 - GetCurrentClusterNodeId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCurrentClusterNodeId macro


## -description


Returns the unique identifier of the current cluster 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes">node</a>.


## -parameters




#### - _lpszNodeId_ [out]

This parameter points to a buffer that receives the unique ID of <i>hNode</i>, including 
       the terminating <b>NULL</b> character.


#### - _lpcchName_ [in, out]

On input, pointer to the count of characters in the buffer pointed to by the 
       <i>lpszNodeId</i> parameter, including the <b>NULL</b> terminator. On 
       output, pointer to the count of characters stored in the buffer excluding the <b>NULL</b> 
       terminator.


#### - lpcchName [in, out]

On input, pointer to the count of characters in the buffer pointed to by the 
       <i>lpszNodeId</i> parameter, including the <b>NULL</b> terminator. On 
       output, pointer to the count of characters stored in the buffer excluding the <b>NULL</b> 
       terminator.


#### - lpszNodeId [out]

This parameter points to a buffer that receives the unique ID of <i>hNode</i>, including 
       the terminating <b>NULL</b> character.


## -remarks



Note that <i>lpcchName</i> refers to a count of characters and not a count of bytes, and 
     that the returned size does not include the terminating <b>NULL</b> in the count. For more information on sizing 
     buffers, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/data-size-conventions">Data Size Conventions</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-getclusternodeid">GetClusterNodeId</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/node-management-functions">Node Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-openclusternode">OpenClusterNode</a>
 

 

