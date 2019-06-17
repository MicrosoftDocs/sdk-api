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
f1_keywords: ["resapi/ExtendControlCall"]
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
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-control-codes">Resource Control Codes</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-dll-callback-functions">Resource DLL Callback Functions</a>
 

 

