---
UID: NC:resapi.PEXTEND_RES_TYPE_CONTROL_CALL
title: PEXTEND_RES_TYPE_CONTROL_CALL
author: windows-sdk-content
description: Extends the timeout for a call to a resource type control code. The PEXTEND_RES_TYPE_CONTROL_CALL type defines a pointer to this function.
old-location: mscs\extendtypecontrolcall.htm
old-project: mscs
ms.assetid: 90E9A989-D281-440D-8441-02086841356E
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ExtendResTypeControlCall, ExtendResTypeControlCall callback, ExtendResTypeControlCall callback function [Failover Cluster], PEXTEND_RES_TYPE_CONTROL_CALL, PEXTEND_RES_TYPE_CONTROL_CALL callback function [Failover Cluster], mscs.extendtypecontrolcall, resapi/ExtendResTypeControlCall, resapi/PEXTEND_RES_TYPE_CONTROL_CALL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
 - ExtendResTypeControlCall
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PEXTEND_RES_TYPE_CONTROL_CALL callback function


## -description


Extends the timeout for a call to a resource type control code. The <b>PEXTEND_RES_TYPE_CONTROL_CALL</b> type defines a pointer to this function.


## -parameters




### -param context [in]

The context to the resource type control code that was called.


### -param newTimeoutInMs [in]

The new timeout, in milliseconds.


## -returns



<b>ERROR_SUCCESS</b> if the operation is successful; otherwise, a system error code.




## -see-also




<a href="https://msdn.microsoft.com/6c7de7e6-a0f5-4308-8cf3-21968bd339a4">Resource DLL Callback Functions</a>



<a href="https://msdn.microsoft.com/a854829d-ed05-40a0-b7c8-c3e5ab888220">Resource Type Control Codes</a>
 

 

