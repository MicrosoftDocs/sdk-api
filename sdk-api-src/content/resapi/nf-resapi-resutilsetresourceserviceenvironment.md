---
UID: NF:resapi.ResUtilSetResourceServiceEnvironment
title: ResUtilSetResourceServiceEnvironment function
author: windows-sdk-content
description: Adjusts the environment data for a service so that the service uses a cluster network name to identify its location. This function must be called from a resource DLL. The PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT type defines a pointer to this function.
old-location: mscs\resutilsetresourceserviceenvironment.htm
tech.root: mscs
ms.assetid: 607695f5-c542-40b8-922f-b76de6859ca7
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT, PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT function [Failover Cluster], ResUtilSetResourceServiceEnvironment, ResUtilSetResourceServiceEnvironment function [Failover Cluster], _wolf_resutilsetresourceserviceenvironment, mscs.resutilsetresourceserviceenvironment, resapi/PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT, resapi/ResUtilSetResourceServiceEnvironment
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilSetResourceServiceEnvironment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ResUtilSetResourceServiceEnvironment
: 
---

# ResUtilSetResourceServiceEnvironment function


## -description


Adjusts the environment data for a <a href="s_gly.htm">service</a> so that the service uses a cluster network name to identify its location. This function must be called from a  <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a>. The <b>PRESUTIL_SET_RESOURCE_SERVICE_ENVIRONMENT</b> type defines a pointer to this function.


## -parameters




### -param pszServiceName [in]

Pointer a null-terminated Unicode string containing the name of the service.


### -param hResource [in]

Resource handle for the service obtained from  <a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>.


### -param pfnLogEvent [in]

Pointer to the  <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> entry point function of the resource DLL managing the service.


### -param hResourceHandle [in]

Resource handle required by the  <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> entry point function. Use the handle passed to the DLL in the  <a href="https://msdn.microsoft.com/0a5c10c5-0380-4638-b49d-396be3b3c0dd">Open</a> entry point function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



<b>ResUtilSetResourceServiceEnvironment</b> calls  <a href="https://msdn.microsoft.com/683235ac-153d-4442-915e-e1bf9b5e8810">ResUtilGetEnvironmentWithNetName</a> and stores the resulting environment block in a registry entry for the service. For more information about the effects of the environment block, see  <b>ResUtilGetEnvironmentWithNetName</b>.

If your resource DLL manages a service, create a worker thread and use  <a href="https://msdn.microsoft.com/5400ed27-4299-470c-bfce-bc91d09f1708">ResUtilSetResourceServiceStartParameters</a> and  <b>ResUtilSetResourceServiceEnvironment</b> when bringing the service online.

Do not call  <b>ResUtilSetResourceServiceEnvironment</b> from any resource DLL entry point function.  <b>ResUtilSetResourceServiceEnvironment</b> can safely be called from a worker thread. For more information, see  <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/683235ac-153d-4442-915e-e1bf9b5e8810">ResUtilGetEnvironmentWithNetName</a>
 

 

