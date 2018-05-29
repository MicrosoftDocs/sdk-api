---
UID: NC:resapi.PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT
title: PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT
author: windows-sdk-content
description: Removes the environment data from a service. This function must be called from a resource DLL. The PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT type defines a pointer to this function.
old-location: mscs\resutilremoveresourceserviceenvironment.htm
old-project: MsCS
ms.assetid: e0e3ea2d-9cf2-40f6-a3a8-fdcacb63479c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT, PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT callback, PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT callback function [Failover Cluster], mscs.resutilremoveresourceserviceenvironment, resapi/PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT
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
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT callback function


## -description


Removes the environment data from a <a href="https://msdn.microsoft.com/library/windows/hardware/mt269769">service</a>. This function must be called from a <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a>. The <b>PRESUTIL_REMOVE_RESOURCE_SERVICE_ENVIRONMENT</b> type defines a pointer to this function.


## -parameters




### -param pszServiceName [in]

Pointer  to a null-terminated Unicode string  that contains the name of the service.


### -param pfnLogEvent [in]

Pointer to the  <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> entry point function of the resource DLL  that manages  the service.


### -param hResourceHandle [in]

Resource handle  that  the  <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> entry point function  requires. Use the handle passed to the DLL in the  <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> entry point function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -see-also




<a href="https://msdn.microsoft.com/683235ac-153d-4442-915e-e1bf9b5e8810">ResUtilGetEnvironmentWithNetName</a>
 

 

