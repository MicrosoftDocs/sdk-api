---
UID: NC:resapi.PEXTEND_RES_TYPE_CONTROL_CALL
title: PEXTEND_RES_TYPE_CONTROL_CALL (resapi.h)
description: Extends the timeout for a call to a resource type control code. The PEXTEND_RES_TYPE_CONTROL_CALL type defines a pointer to this function.
helpviewer_keywords: ["ExtendResTypeControlCall","ExtendResTypeControlCall callback","ExtendResTypeControlCall callback function [Failover Cluster]","PEXTEND_RES_TYPE_CONTROL_CALL","PEXTEND_RES_TYPE_CONTROL_CALL callback function [Failover Cluster]","mscs.extendtypecontrolcall","resapi/ExtendResTypeControlCall","resapi/PEXTEND_RES_TYPE_CONTROL_CALL"]
old-location: mscs\extendtypecontrolcall.htm
tech.root: MsCS
ms.assetid: 90E9A989-D281-440D-8441-02086841356E
ms.date: 12/05/2018
ms.keywords: ExtendResTypeControlCall, ExtendResTypeControlCall callback, ExtendResTypeControlCall callback function [Failover Cluster], PEXTEND_RES_TYPE_CONTROL_CALL, PEXTEND_RES_TYPE_CONTROL_CALL callback function [Failover Cluster], mscs.extendtypecontrolcall, resapi/ExtendResTypeControlCall, resapi/PEXTEND_RES_TYPE_CONTROL_CALL
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PEXTEND_RES_TYPE_CONTROL_CALL
 - resapi/PEXTEND_RES_TYPE_CONTROL_CALL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - ExtendResTypeControlCall
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

<a href="/previous-versions/windows/desktop/mscs/resource-dll-callback-functions">Resource DLL Callback Functions</a>



<a href="/previous-versions/windows/desktop/mscs/resource-type-control-codes">Resource Type Control Codes</a>