---
UID: NC:resapi.PSET_RESOURCE_LOCKED_MODE_ROUTINE
title: PSET_RESOURCE_LOCKED_MODE_ROUTINE
author: windows-driver-content
description: Reports that locked mode was configured for a resource.
old-location: mscs\setresourcelockedmode.htm
old-project: MsCS
ms.assetid: 000D127C-7BDE-4FC1-984E-2EE805E603FC
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PSET_RESOURCE_LOCKED_MODE_ROUTINE, PSET_RESOURCE_LOCKED_MODE_ROUTINE callback function [Failover Cluster], SetResourceLockedMode, SetResourceLockedMode callback, SetResourceLockedMode callback function [Failover Cluster], mscs.setresourcelockedmode, resapi/PSET_RESOURCE_LOCKED_MODE_ROUTINE, resapi/SetResourceLockedMode
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
-	SetResourceLockedMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PSET_RESOURCE_LOCKED_MODE_ROUTINE callback function


## -description


Reports that  locked mode was configured for a resource.


## -parameters




### -param ResourceHandle [in]

A handle to the resource to configure.


### -param LockedModeEnabled [in]

<b>TRUE</b> to enable locked mode; otherwise <b>FALSE</b>.


### -param LockedModeReason [in]

A flag that specifies the reason that locked mode was configured.


## -returns



Returns <b>ERROR_SUCCESS</b> (0), if the operation succeeds; otherwise returns a system error code.




## -see-also




<a href="https://msdn.microsoft.com/6c7de7e6-a0f5-4308-8cf3-21968bd339a4">Resource DLL Callback Functions</a>
 

 

