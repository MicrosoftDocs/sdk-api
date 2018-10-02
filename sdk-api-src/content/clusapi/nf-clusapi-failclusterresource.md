---
UID: NF:clusapi.FailClusterResource
title: FailClusterResource function
author: windows-sdk-content
description: Initiates a resource failure.
old-location: mscs\failclusterresource.htm
tech.root: MsCS
ms.assetid: fcf0226e-4dd0-4c13-86eb-bc87e461234c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FailClusterResource, FailClusterResource function [Failover Cluster], PCLUSAPI_FAIL_CLUSTER_RESOURCE, PCLUSAPI_FAIL_CLUSTER_RESOURCE function [Failover Cluster], _wolf_failclusterresource, clusapi/FailClusterResource, clusapi/PCLUSAPI_FAIL_CLUSTER_RESOURCE, mscs.failclusterresource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - FailClusterResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FailClusterResource function


## -description


Initiates a  <a href="https://msdn.microsoft.com/en-us/library/Aa372255(v=VS.85).aspx">resource failure</a>. The <b>PCLUSAPI_FAIL_CLUSTER_RESOURCE</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to the  <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a> that is the target of the failure.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



The resource identified by <i>hResource</i> is treated as inoperable, causing the <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a> to initiate the same  <a href="https://msdn.microsoft.com/en-us/library/Aa369573(v=VS.85).aspx">failover</a> process that would result if the resource had actually failed. Applications call the  <b>FailClusterResource</b> function to test their policies for restarting resources and  <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">groups</a>.

Do not call  <b>FailClusterResource</b> from a resource DLL. For more information, see  <a href="https://msdn.microsoft.com/en-us/library/Aa369588(v=VS.85).aspx">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

