---
UID: NF:clusapi.OfflineClusterGroup
title: OfflineClusterGroup function (clusapi.h)
description: Takes a group offline.
helpviewer_keywords: ["OfflineClusterGroup","OfflineClusterGroup function [Failover Cluster]","PCLUSAPI_OFFLINE_CLUSTER_GROUP","PCLUSAPI_OFFLINE_CLUSTER_GROUP function [Failover Cluster]","_wolf_offlineclustergroup","clusapi/OfflineClusterGroup","clusapi/PCLUSAPI_OFFLINE_CLUSTER_GROUP","mscs.offlineclustergroup"]
old-location: mscs\offlineclustergroup.htm
tech.root: MsCS
ms.assetid: 465e9eac-6286-4955-a11c-a515c64230da
ms.date: 12/05/2018
ms.keywords: OfflineClusterGroup, OfflineClusterGroup function [Failover Cluster], PCLUSAPI_OFFLINE_CLUSTER_GROUP, PCLUSAPI_OFFLINE_CLUSTER_GROUP function [Failover Cluster], _wolf_offlineclustergroup, clusapi/OfflineClusterGroup, clusapi/PCLUSAPI_OFFLINE_CLUSTER_GROUP, mscs.offlineclustergroup
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OfflineClusterGroup
 - clusapi/OfflineClusterGroup
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
 - OfflineClusterGroup
---

# OfflineClusterGroup function


## -description

Takes a  <a href="/previous-versions/windows/desktop/mscs/groups">group</a> offline. The <b>PCLUSAPI_OFFLINE_CLUSTER_GROUP</b> type defines a pointer to this function.

## -parameters

### -param hGroup [in]

Handle to the group to be taken offline.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is one of the possible error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The operation is in progress.

</td>
</tr>
</table>

## -remarks

Do not call  <b>OfflineClusterGroup</b> from a resource DLL. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-onlineclustergroup">OnlineClusterGroup</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclustergroup">OpenClusterGroup</a>