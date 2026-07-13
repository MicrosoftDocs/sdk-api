---
UID: NF:clusapi.OnlineClusterResourceEx
title: OnlineClusterResourceEx function (clusapi.h)
description: Brings an offline or failed resource online. (OnlineClusterResourceEx)
helpviewer_keywords: ["CLUSAPI_GROUP_ONLINE_IGNORE_RESOURCE_STATUS","CLUSAPI_RESOURCE_ONLINE_BEST_POSSIBLE_NODE","CLUSAPI_RESOURCE_ONLINE_DO_NOT_UPDATE_PERSISTENT_STATE","CLUSAPI_RESOURCE_ONLINE_NECESSARY_FOR_QUORUM","OnlineClusterResourceEx","OnlineClusterResourceEx function [Failover Cluster]","clusapi/OnlineClusterResourceEx","mscs.onlineclusterresourceex"]
old-location: mscs\onlineclusterresourceex.htm
tech.root: MsCS
ms.assetid: 8A41D266-0FBD-4063-9C79-E22924129989
ms.date: 12/05/2018
ms.keywords: CLUSAPI_GROUP_ONLINE_IGNORE_RESOURCE_STATUS, CLUSAPI_RESOURCE_ONLINE_BEST_POSSIBLE_NODE, CLUSAPI_RESOURCE_ONLINE_DO_NOT_UPDATE_PERSISTENT_STATE, CLUSAPI_RESOURCE_ONLINE_NECESSARY_FOR_QUORUM, OnlineClusterResourceEx, OnlineClusterResourceEx function [Failover Cluster], clusapi/OnlineClusterResourceEx, mscs.onlineclusterresourceex
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - OnlineClusterResourceEx
 - clusapi/OnlineClusterResourceEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - OnlineClusterResourceEx
---

# OnlineClusterResourceEx function


## -description

Brings an offline or failed  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> online.

## -parameters

### -param hResource [in]

The handle to the resource to bring online.

### -param dwOnlineFlags [in]

A flag that specifies settings for the resource that is to be brought online.



#### CLUSAPI_GROUP_ONLINE_IGNORE_RESOURCE_STATUS (0x00000001)

The server is to ignore locked mode for the resource.



#### CLUSAPI_RESOURCE_ONLINE_DO_NOT_UPDATE_PERSISTENT_STATE (0x00000002)

Do not update the persistent state of the resource.



#### CLUSAPI_RESOURCE_ONLINE_NECESSARY_FOR_QUORUM (0x00000004)

The resource must be brought online to maintain a quorum.



#### CLUSAPI_RESOURCE_ONLINE_BEST_POSSIBLE_NODE (0x00000008)

The cluster service is to determine the node that will host the resource when it is brought online.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This value is not supported before Windows Server 2016.



#### 0

The server is  not to  ignore locked mode for the resource.

### -param lpInBuffer [in, optional]

A pointer to the input buffer that receives instructions for the operation. The <i>lpInBuffer</i>  parameter is formatted as a property list.

### -param cbInBufferSize [in]

The size of <i>lpInBuffer</i>, in bytes.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is a possible error code.

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
The resource or one of the resources that  it depends on has returned <b>ERROR_IO_PENDING</b> from its  <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a> entry point function.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>
