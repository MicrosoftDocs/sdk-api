---
UID: NC:resapi.PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME
title: PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME
author: windows-sdk-content
description: Adjusts environment data for a resource so that the resource uses a cluster network name to identify its location.
old-location: mscs\resutilgetenvironmentwithnetname.htm
old-project: MsCS
ms.assetid: 683235ac-153d-4442-915e-e1bf9b5e8810
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME, PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME callback, PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME callback function [Failover Cluster], _wolf_resutilgetenvironmentwithnetname, mscs.resutilgetenvironmentwithnetname, resapi/PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
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
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME callback function


## -description


Adjusts environment data for a  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> so that the resource uses a cluster network name to identify its location. The resource must be dependent on a  <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a> resource. The <b>PRESUTIL_GET_ENVIRONMENT_WITH_NET_NAME</b> type defines a pointer to this function.


## -parameters




### -param hResource [in]

Handle to a resource that depends on a Network Name resource.


## -returns



If the operations succeeds, the function returns a pointer to the environment block.

If the operation fails, 
the function returns <b>NULL</b>. For more information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The  <i>ResUtilGetEnvironmentWithNetName</i> function appends environment variables to the current environment block. Pass the returned environment block to  <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> when starting the resource to achieve the following effects:

<ul>
<li>Clients and the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> can locate the resource by using the name of the Network Name resource.</li>
<li>If the resource calls <a href="https://msdn.microsoft.com/8ca3e611-e5fb-4909-adf6-98eb8552c9e1">GetComputerName</a>, <a href="https://msdn.microsoft.com/eae3f75d-7ec7-42ae-b207-e3ebaa33346e">GetComputerNameEx</a>, or <a href="https://msdn.microsoft.com/2526ecb5-927b-40c8-8d8f-919e7986ff05">gethostbyname</a>, the network name will be returned regardless of which node is currently hosting the resource.</li>
</ul>
If the resource identified by <i>hResource</i> is not dependent on a Network Name resource,  <i>ResUtilGetEnvironmentWithNetName</i> returns <b>NULL</b>.

Use  <a href="https://msdn.microsoft.com/196f347e-2b2f-4bb1-a86c-b2a73881ed65">ResUtilFreeEnvironment</a> to destroy the environment block.

Do not call  <i>ResUtilGetEnvironmentWithNetName</i> from any resource DLL entry point function.  <i>ResUtilGetEnvironmentWithNetName</i> can safely be called from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/607695f5-c542-40b8-922f-b76de6859ca7">ResUtilSetResourceServiceEnvironment</a>
 

 

