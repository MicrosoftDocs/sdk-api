---
UID: NF:clusapi.CloseClusterGroupSet
title: CloseClusterGroupSet function (clusapi.h)
description: Closes a groupset handle returned from OpenClusterGroupSet.
helpviewer_keywords: ["CloseClusterGroupSet","CloseClusterGroupSet function [Failover Cluster]","PCLUSAPI_CLOSE_CLUSTER_GROUP_SET","PCLUSAPI_CLOSE_CLUSTER_GROUP_SET function [Failover Cluster]","clusapi/CloseClusterGroupSet","clusapi/PCLUSAPI_CLOSE_CLUSTER_GROUP_SET","mscs.closeclustergroupcollection"]
old-location: mscs\closeclustergroupcollection.htm
tech.root: MsCS
ms.assetid: 017f0c40-023d-4b22-90ec-037122718830
ms.date: 12/05/2018
ms.keywords: CloseClusterGroupSet, CloseClusterGroupSet function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER_GROUP_SET, PCLUSAPI_CLOSE_CLUSTER_GROUP_SET function [Failover Cluster], clusapi/CloseClusterGroupSet, clusapi/PCLUSAPI_CLOSE_CLUSTER_GROUP_SET, mscs.closeclustergroupcollection
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CloseClusterGroupSet
 - clusapi/CloseClusterGroupSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - CloseClusterGroupSet
---

# CloseClusterGroupSet function


## -description

Closes a groupset handle returned from <a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroupset">OpenClusterGroupSet</a>.

## -parameters

### -param hGroupSet [in]

The handle to close

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The operation was not successful. For more information about the error, call the function  <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
</table>