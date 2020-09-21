---
UID: NF:clusapi.FailClusterResource
title: FailClusterResource function (clusapi.h)
description: Initiates a resource failure.
helpviewer_keywords: ["FailClusterResource","FailClusterResource function [Failover Cluster]","PCLUSAPI_FAIL_CLUSTER_RESOURCE","PCLUSAPI_FAIL_CLUSTER_RESOURCE function [Failover Cluster]","_wolf_failclusterresource","clusapi/FailClusterResource","clusapi/PCLUSAPI_FAIL_CLUSTER_RESOURCE","mscs.failclusterresource"]
old-location: mscs\failclusterresource.htm
tech.root: MsCS
ms.assetid: fcf0226e-4dd0-4c13-86eb-bc87e461234c
ms.date: 12/05/2018
ms.keywords: FailClusterResource, FailClusterResource function [Failover Cluster], PCLUSAPI_FAIL_CLUSTER_RESOURCE, PCLUSAPI_FAIL_CLUSTER_RESOURCE function [Failover Cluster], _wolf_failclusterresource, clusapi/FailClusterResource, clusapi/PCLUSAPI_FAIL_CLUSTER_RESOURCE, mscs.failclusterresource
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
 - FailClusterResource
 - clusapi/FailClusterResource
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
 - FailClusterResource
---

# FailClusterResource function


## -description

Initiates a  <a href="/previous-versions/windows/desktop/mscs/resource-failure">resource failure</a>. The <b>PCLUSAPI_FAIL_CLUSTER_RESOURCE</b> type defines a pointer to this function.

## -parameters

### -param hResource [in]

Handle to the  <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> that is the target of the failure.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="/windows/desktop/Debug/system-error-codes">system error code</a>.

## -remarks

The resource identified by <i>hResource</i> is treated as inoperable, causing the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a> to initiate the same  <a href="/previous-versions/windows/desktop/mscs/failover">failover</a> process that would result if the resource had actually failed. Applications call the  <b>FailClusterResource</b> function to test their policies for restarting resources and  <a href="/previous-versions/windows/desktop/mscs/groups">groups</a>.

Do not call  <b>FailClusterResource</b> from a resource DLL. For more information, see  <a href="/previous-versions/windows/desktop/mscs/function-calls-to-avoid-in-resource-dlls">Function Calls to Avoid in Resource DLLs</a>.

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>