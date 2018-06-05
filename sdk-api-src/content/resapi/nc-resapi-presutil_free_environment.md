---
UID: NC:resapi.PRESUTIL_FREE_ENVIRONMENT
title: PRESUTIL_FREE_ENVIRONMENT
author: windows-sdk-content
description: Destroys the environment variable block created with ResUtilGetEnvironmentWithNetName. The PRESUTIL_FREE_ENVIRONMENT type defines a pointer to this function.
old-location: mscs\resutilfreeenvironment.htm
old-project: MsCS
ms.assetid: 196f347e-2b2f-4bb1-a86c-b2a73881ed65
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PRESUTIL_FREE_ENVIRONMENT, PRESUTIL_FREE_ENVIRONMENT callback, PRESUTIL_FREE_ENVIRONMENT callback function [Failover Cluster], _wolf_resutilfreeenvironment, mscs.resutilfreeenvironment, resapi/PRESUTIL_FREE_ENVIRONMENT
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
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PRESUTIL_FREE_ENVIRONMENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PRESUTIL_FREE_ENVIRONMENT callback function


## -description


Destroys the environment variable block created with  <a href="https://msdn.microsoft.com/683235ac-153d-4442-915e-e1bf9b5e8810">ResUtilGetEnvironmentWithNetName</a>. The <b>PRESUTIL_FREE_ENVIRONMENT</b> type defines a pointer to this function.


## -parameters




### -param lpEnvironment [in]

Pointer to the environment variable block returned from  <a href="https://msdn.microsoft.com/683235ac-153d-4442-915e-e1bf9b5e8810">ResUtilGetEnvironmentWithNetName</a>.


## -returns



This function has no return values.




## -see-also




<a href="https://msdn.microsoft.com/683235ac-153d-4442-915e-e1bf9b5e8810">ResUtilGetEnvironmentWithNetName</a>
 

 

