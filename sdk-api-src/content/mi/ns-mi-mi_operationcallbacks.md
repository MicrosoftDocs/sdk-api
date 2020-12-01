---
UID: NS:mi._MI_OperationCallbacks
title: MI_OperationCallbacks (mi.h)
description: Structure that holds all callback function pointers for carrying out operations.
helpviewer_keywords: ["MI_OperationCallbacks","MI_OperationCallbacks structure [Windows Management Infrastructure (MI)]","mi/MI_OperationCallbacks","wmi._mi_operationcallbacks","wmi_v2.mi_operationcallbacks"]
old-location: wmi_v2\mi_operationcallbacks.htm
tech.root: wmi_v2
ms.assetid: f56954bf-c1aa-408b-bc45-0faf2a99b381
ms.date: 12/05/2018
ms.keywords: MI_OperationCallbacks, MI_OperationCallbacks structure [Windows Management Infrastructure (MI)], mi/MI_OperationCallbacks, wmi._mi_operationcallbacks, wmi_v2.mi_operationcallbacks
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MI_OperationCallbacks
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_OperationCallbacks
 - mi/_MI_OperationCallbacks
 - MI_OperationCallbacks
 - mi/MI_OperationCallbacks
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_OperationCallbacks
---

# MI_OperationCallbacks structure


## -description

Structure that holds all callback function pointers for carrying out operations.

## -struct-fields

### -field callbackContext

A client specific context that is passed to all the callbacks. This is used to correlate the callback to the associated operation. This value will be passed to any operation callbacks.

### -field promptUser

Optional callback to handle prompt user requests from the server.

### -field writeError

Optional callback to receive write error messages from the server.

### -field writeMessage

Optional callback to receive write messages from the server.

### -field writeProgress

Optional callback to receive progress reports from the server.

### -field instanceResult

Optional instance callback to get asynchronous results from an operation.  If this is not specified and the operation is an instance operation, then the client will need to use the synchronous APIs to retrieve the results.

### -field indicationResult

Optional instance callback to get indication (subscribe) results from an operation.  If this is not specified and the operation is an instance operation, then the client will need to use the synchronous APIs to retrieve the results.

### -field classResult

Optional instance callback to get classes and class options from an operation.  If this is not specified and the operation is an instance operation, then the client will need to use the synchronous APIs to retrieve the results.

### -field streamedParameterResult

Optional callback to get streamed parameter results from method invocation operations.

## -remarks

All PowerShell Semantics and streamed result callbacks are optional;  include the callbacks 
 you want to receive. If the associated operation callback for the operation
is not set, i.e. set to <b>NULL</b>, the operation will be carried out synchronously. The client must call into the appropriate MI_Operation function to receive the results. The result callbacks will continue to be called until the moreResults field is equal to MI_FALSE.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dn792325(v=vs.85)">MI_OperationCallback_Class</a>



<a href="/previous-versions/windows/desktop/legacy/dn792326(v=vs.85)">MI_OperationCallback_Indication</a>



<a href="/previous-versions/windows/desktop/legacy/dn792327(v=vs.85)">MI_OperationCallback_Instance</a>



<a href="/previous-versions/windows/desktop/legacy/dn792328(v=vs.85)">MI_OperationCallback_PromptUser</a>



<a href="/previous-versions/windows/desktop/legacy/dn792329(v=vs.85)">MI_OperationCallback_StreamedParameter</a>



<a href="/previous-versions/windows/desktop/legacy/dn792330(v=vs.85)">MI_OperationCallback_WriteError</a>



<a href="/previous-versions/windows/desktop/legacy/dn759645(v=vs.85)">MI_OperationCallback_WriteMessage</a>



<a href="/previous-versions/windows/desktop/legacy/dn759646(v=vs.85)">MI_OperationCallback_WriteProgress</a>