---
UID: NF:resapi.ResUtilSetResourceServiceStartParameters
title: ResUtilSetResourceServiceStartParameters function (resapi.h)
author: windows-sdk-content
description: Adjusts the start parameters of a specified service so that it will operate correctly as a cluster resource. It must be called from a resource DLL. The PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS type defines a pointer to this function.
old-location: mscs\resutilsetresourceservicestartparameters.htm
tech.root: MsCS
ms.assetid: 5400ed27-4299-470c-bfce-bc91d09f1708
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS, PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS function [Failover Cluster], ResUtilSetResourceServiceStartParameters, ResUtilSetResourceServiceStartParameters function [Failover Cluster], _wolf_resutilsetresourceservicestartparameters, mscs.resutilsetresourceservicestartparameters, resapi/PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS, resapi/ResUtilSetResourceServiceStartParameters
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
 - ResUtilSetResourceServiceStartParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResUtilSetResourceServiceStartParameters function


## -description


Adjusts the start parameters of a specified <a href="https://msdn.microsoft.com/en-us/library/Aa372937(v=VS.85).aspx">service</a> so that it will operate correctly as a cluster  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. It must be called from a  <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a>. The <b>PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS</b> type defines a pointer to this function.


## -parameters




### -param pszServiceName [in]

Pointer to a null-terminated Unicode string specifying the name of the service.


### -param schSCMHandle [in]

Handle to the Service Control Manager (SCM) or <b>NULL</b>. If <b>NULL</b>, the function will attempt to open a handle to the SCM.


### -param phService [in, out]

On input, a <b>NULL</b> service handle. On output, handle to the specified service if the call was successful, otherwise <b>NULL</b>.


### -param pfnLogEvent [in]

Pointer to the  <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> entry point function of the resource DLL managing the service.


### -param hResourceHandle [in]

Resource handle required by the  <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> entry point function. Use the handle passed to the DLL in the  <a href="https://msdn.microsoft.com/0a5c10c5-0380-4638-b49d-396be3b3c0dd">Open</a> entry point function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



<b>ResUtilSetResourceServiceStartParameters</b> verifies that the service is not disabled, changes the service configuration to manual start and prevents the service from restarting in response to failure. This allows the <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a> and the resource DLL to control the service.

If your resource DLL manages a service, use  <b>ResUtilSetResourceServiceStartParameters</b> and  <a href="https://msdn.microsoft.com/607695f5-c542-40b8-922f-b76de6859ca7">ResUtilSetResourceServiceEnvironment</a> before bringing the service online.




## -see-also




<a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a>



<a href="https://msdn.microsoft.com/b406ef44-0622-4625-a6cf-462b6ea6018d">Online</a>



<a href="https://msdn.microsoft.com/0a5c10c5-0380-4638-b49d-396be3b3c0dd">Open</a>



<a href="https://msdn.microsoft.com/607695f5-c542-40b8-922f-b76de6859ca7">ResUtilSetResourceServiceEnvironment</a>
 

 

