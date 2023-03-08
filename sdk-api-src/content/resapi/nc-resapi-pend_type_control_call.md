---
UID: NC:resapi.PEND_TYPE_CONTROL_CALL
title: PEND_TYPE_CONTROL_CALL (resapi.h)
description: Called when a resource type control code operation completes. The PEND_TYPE_CONTROL_CALL type defines a pointer to this function.
helpviewer_keywords: ["EndTypeControlCall","EndTypeControlCall callback","EndTypeControlCall callback function [Failover Cluster]","PEND_TYPE_CONTROL_CALL","PEND_TYPE_CONTROL_CALL callback function [Failover Cluster]","mscs.endtypecontrolcall","resapi/EndTypeControlCall","resapi/PEND_TYPE_CONTROL_CALL"]
old-location: mscs\endtypecontrolcall.htm
tech.root: MsCS
ms.assetid: EF3C2DFA-2B8A-4709-A6B6-56427C0C00A5
ms.date: 12/05/2018
ms.keywords: EndTypeControlCall, EndTypeControlCall callback, EndTypeControlCall callback function [Failover Cluster], PEND_TYPE_CONTROL_CALL, PEND_TYPE_CONTROL_CALL callback function [Failover Cluster], mscs.endtypecontrolcall, resapi/EndTypeControlCall, resapi/PEND_TYPE_CONTROL_CALL
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
 - PEND_TYPE_CONTROL_CALL
 - resapi/PEND_TYPE_CONTROL_CALL
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - EndTypeControlCall callback
---

# PEND_TYPE_CONTROL_CALL callback function


## -description

Called when a resource type control code operation completes. The <b>PEND_TYPE_CONTROL_CALL</b> type defines a pointer to this function.

## -parameters

### -param context

### -param status [in]

The context of the call to the resource type control code.

The status of the operation.


#### - resCallId [in]

Not supported.

<b>Windows Server 2012 R2:  </b>TBD

## -returns

<b>ERROR_SUCCESS</b> if the operation is successful; otherwise, a system error code.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-callback-functions">Resource DLL Callback Functions</a>