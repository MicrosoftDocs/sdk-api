---
UID: NC:resapi.PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX
title: PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX
author: windows-driver-content
description: Adjusts the start parameters of a specified service so that it operates correctly as a cluster resource. It must be called from a resource DLL. The PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX type defines a pointer to this function.
old-location: mscs\resutilsetresourceservicestartparametersex.htm
old-project: MsCS
ms.assetid: 12F1AD70-4B6C-4920-855C-C55C8F423C69
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX, PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX callback function [Failover Cluster], mscs.resutilsetresourceservicestartparametersex, resapi/PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
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
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX callback


## -description


Adjusts the start parameters of a specified <a href="https://msdn.microsoft.com/library/windows/hardware/mt269769">service</a> so that it  operates  correctly as a cluster  <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. It must be called from a  <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a>. The <b>PRESUTIL_SET_RESOURCE_SERVICE_START_PARAMETERS_EX</b> type defines a pointer to this function.


## -parameters




### -param pszServiceName [in]

A pointer to a null-terminated Unicode string that specifies  the name of the service.


### -param schSCMHandle [in]

A handle to the Service Control Manager (SCM) or <b>NULL</b>. If <b>NULL</b>, the function  attempts to open a handle to the SCM.


### -param phService [in, out]

On input, a <b>NULL</b> service handle. On output, handle to the specified service if the call was successful; otherwise <b>NULL</b>.


### -param dwDesiredAccess [in]

The requested access privileges. This  might  be any combination of <b>GENERIC_READ</b> (0x80000000), <b>GENERIC_ALL</b> (0x10000000), or <b>MAXIMUM_ALLOWED</b> (0x02000000). If this value is zero (0),  an undefined error might  be returned. Using <b>GENERIC_ALL</b> is the same as calling <a href="https://msdn.microsoft.com/5400ed27-4299-470c-bfce-bc91d09f1708">ResUtilSetResourceServiceStartParameters</a>.


### -param pfnLogEvent [in]

A pointer to the  <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> entry point function of the resource DLL that manages  the service.


### -param hResourceHandle [in]

A resource handle that is required by the  <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> entry point function. Use the handle that is passed to the DLL in the  <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> entry point function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



<i>ResUtilSetResourceServiceStartParametersEx</i> verifies that the service is not disabled, changes the service configuration to manual start, and prevents the service from restarting in response to failure. This  enables  the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and the resource DLL to control the service.

If your resource DLL manages a service, use  <i>ResUtilSetResourceServiceStartParametersEx</i> and  <a href="https://msdn.microsoft.com/607695f5-c542-40b8-922f-b76de6859ca7">ResUtilSetResourceServiceEnvironment</a> before you  bring the service online.




## -see-also




<a href="https://msdn.microsoft.com/5400ed27-4299-470c-bfce-bc91d09f1708">ResUtilSetResourceServiceStartParameters</a>



<a href="https://msdn.microsoft.com/16fcc65f-81b3-4126-a56e-4aaee3099b8c">Service Utility Functions</a>
 

 

