---
UID: NC:clusapi.PCLUSAPI_FAIL_CLUSTER_RESOURCE
title: PCLUSAPI_FAIL_CLUSTER_RESOURCE
author: windows-sdk-content
description: Initiates a resource failure.
old-location: mscs\failclusterresource.htm
old-project: MsCS
ms.assetid: fcf0226e-4dd0-4c13-86eb-bc87e461234c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSAPI_FAIL_CLUSTER_RESOURCE, PCLUSAPI_FAIL_CLUSTER_RESOURCE callback, PCLUSAPI_FAIL_CLUSTER_RESOURCE callback function [Failover Cluster], _wolf_failclusterresource, clusapi/PCLUSAPI_FAIL_CLUSTER_RESOURCE, mscs.failclusterresource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSAPI_FAIL_CLUSTER_RESOURCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_FAIL_CLUSTER_RESOURCE callback function


## -description


Initiates a  <a href="https://msdn.microsoft.com/f18644d1-63ec-4920-b703-a3f149684508">resource failure</a>. The <b>PCLUSAPI_FAIL_CLUSTER_RESOURCE</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> that is the target of the failure.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



The resource identified by <i>hResource</i> is treated as inoperable, causing the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> to initiate the same  <a href="https://msdn.microsoft.com/6722d075-02e0-4817-abc3-dce8951c17da">failover</a> process that would result if the resource had actually failed. Applications call the  <i>FailClusterResource</i> function to test their policies for restarting resources and  <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a>.

Do not call  <i>FailClusterResource</i> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

