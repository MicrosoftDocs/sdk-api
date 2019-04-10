---
UID: NC:resapi.PEXTEND_RES_CONTROL_CALL
title: PEXTEND_RES_CONTROL_CALL (resapi.h)
author: windows-sdk-content
description: Extends the timeout for a call to a resource control code. The PEXTEND_RES_CONTROL_CALL type defines a pointer to this function.
old-location: mscs\extendcontrolcall.htm
tech.root: MsCS
ms.assetid: 79607FE9-96E5-4854-BC92-8FF1C474B3D6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ExtendControlCall, ExtendControlCall callback, ExtendControlCall callback function [Failover Cluster], PEXTEND_RES_CONTROL_CALL, PEXTEND_RES_CONTROL_CALL callback function [Failover Cluster], mscs.extendcontrolcall, resapi/ExtendControlCall, resapi/PEXTEND_RES_CONTROL_CALL
ms.topic: callback
req.header: resapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - ExtendControlCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PEXTEND_RES_CONTROL_CALL callback function


## -description


Extends the timeout for a call to a resource control code. The <b>PEXTEND_RES_CONTROL_CALL</b> type defines a pointer to this function.


## -parameters




### -param context [in]

The context to the resource control code that was called.


### -param newTimeoutInMs [in]

The new timeout, in milliseconds.


## -returns



<b>ERROR_SUCCESS</b> if the operation is successful; otherwise, a system error code.




## -see-also




<a href="https://msdn.microsoft.com/71ec60fd-67ec-4932-983b-f78c6b552954">Resource Control Codes</a>



<a href="https://msdn.microsoft.com/6c7de7e6-a0f5-4308-8cf3-21968bd339a4">Resource DLL Callback Functions</a>
 

 

