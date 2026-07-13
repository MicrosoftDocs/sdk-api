---
UID: NF:clusapi.CanResourceBeDependent
title: CanResourceBeDependent function (clusapi.h)
description: Determines if one resource can be dependent upon another resource.
helpviewer_keywords: ["CanResourceBeDependent","CanResourceBeDependent function [Failover Cluster]","PCLUSAPI_CAN_RESOURCE_BE_DEPENDENT","PCLUSAPI_CAN_RESOURCE_BE_DEPENDENT function [Failover Cluster]","_wolf_canresourcebedependent","clusapi/CanResourceBeDependent","clusapi/PCLUSAPI_CAN_RESOURCE_BE_DEPENDENT","mscs.canresourcebedependent"]
old-location: mscs\canresourcebedependent.htm
tech.root: MsCS
ms.assetid: 974ec036-3dd3-4453-9ce5-029f58d99d81
ms.date: 12/05/2018
ms.keywords: CanResourceBeDependent, CanResourceBeDependent function [Failover Cluster], PCLUSAPI_CAN_RESOURCE_BE_DEPENDENT, PCLUSAPI_CAN_RESOURCE_BE_DEPENDENT function [Failover Cluster], _wolf_canresourcebedependent, clusapi/CanResourceBeDependent, clusapi/PCLUSAPI_CAN_RESOURCE_BE_DEPENDENT, mscs.canresourcebedependent
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
 - CanResourceBeDependent
 - clusapi/CanResourceBeDependent
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
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
api_name:
 - CanResourceBeDependent
---

# CanResourceBeDependent function


## -description

Determines if one  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> can be  <a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependent</a> upon another resource. The <b>PCLUSAPI_CAN_RESOURCE_BE_DEPENDENT</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to the resource in question.

### -param hResourceDependent [in]

Handle to the resource upon which the resource identified by <i>hResource</i> may depend.

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
The resource identified by <i>hResource</i> can depend on the resource identified by <i>hResourceDependent</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The resource identified by <i>hResource</i> cannot depend on the resource identified by <i>hResourceDependent</i>.

</td>
</tr>
</table>

## -remarks

With the  <b>CanResourceBeDependent</b> function, for the resource identified by <i>hResource</i> to be dependent on the resource identified by <i>hResourceDependent</i>, the following must be true:

<ul>
<li>Both resources must be members of the same  <a href="/previous-versions/windows/desktop/mscs/groups">group</a>.</li>
<li>The resource identified by <i>hResourceDependent</i> cannot depend on the resource identified by <i>hResource</i>, either directly or indirectly.</li>
</ul>
Do not call  <b>CanResourceBeDependent</b> from any resource DLL entry point function.  <b>CanResourceBeDependent</b> can safely be called from a worker thread. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

Do not pass LPC and RPC handles to the same function call. Otherwise, the call will raise an RPC exception and can have additional destructive effects. For information on how LPC and RPC handles are created, see  <a href="/previous-versions/windows/desktop/mscs/using-object-handles">Using Object Handles</a> and  <a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-addclusterresourcedependency">AddClusterResourceDependency</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-removeclusterresourcedependency">RemoveClusterResourceDependency</a>