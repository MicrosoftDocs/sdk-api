---
UID: NC:resapi.PEXTEND_RES_TYPE_CONTROL_CALL
title: PEXTEND_RES_TYPE_CONTROL_CALL (resapi.h)
author: windows-sdk-content
description: Extends the timeout for a call to a resource type control code. The PEXTEND_RES_TYPE_CONTROL_CALL type defines a pointer to this function.
old-location: mscs\extendtypecontrolcall.htm
tech.root: MsCS
ms.assetid: 90E9A989-D281-440D-8441-02086841356E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ExtendResTypeControlCall, ExtendResTypeControlCall callback, ExtendResTypeControlCall callback function [Failover Cluster], PEXTEND_RES_TYPE_CONTROL_CALL, PEXTEND_RES_TYPE_CONTROL_CALL callback function [Failover Cluster], mscs.extendtypecontrolcall, resapi/ExtendResTypeControlCall, resapi/PEXTEND_RES_TYPE_CONTROL_CALL
ms.topic: callback
f1_keywords: 
 - "resapi/ExtendResTypeControlCall"
dev_langs:
 - c++
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
 - ExtendResTypeControlCall
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-dll-callback-functions">Resource DLL Callback Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-type-control-codes">Resource Type Control Codes</a>
 

 

