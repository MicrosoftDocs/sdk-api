---
UID: NF:mi.MI_Context_RegisterCancel
title: MI_Context_RegisterCancel function (mi.h)
description: Registers a callback that is invoked when the operation is canceled.
helpviewer_keywords: ["MI_Context_RegisterCancel","MI_Context_RegisterCancel function [Windows Management Infrastructure (MI)]","mi/MI_Context_RegisterCancel","wmi.mi_registercancel","wmi_v2.mi_context_registercancel"]
old-location: wmi_v2\mi_context_registercancel.htm
tech.root: wmi_v2
ms.assetid: 7e6b2016-6ce5-4dcd-b5f4-6e6d24c46f0a
ms.date: 12/05/2018
ms.keywords: MI_Context_RegisterCancel, MI_Context_RegisterCancel function [Windows Management Infrastructure (MI)], mi/MI_Context_RegisterCancel, wmi.mi_registercancel, wmi_v2.mi_context_registercancel
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
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Context_RegisterCancel
 - mi/MI_Context_RegisterCancel
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
 - MI_Context_RegisterCancel
---

# MI_Context_RegisterCancel function


## -description

Registers a callback that is invoked when the operation is canceled.

## -parameters

### -param context [in]

Request context.

### -param callback [in]

Function that will be called if the operation is canceled.

### -param callbackData [in, optional]

Data to be passed to the callback.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

If a provider calls this function multiple times on the same context, only the last callback function will be called. Not all operations canceled on the client will reach the provider. If this is an operation that cannot register the cancellation callback, the function will return an error. This would mean the operation will run to completion. If the operation runs through to completion, the callback function will not be called.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dn792316(v=vs.85)">MI_CancelCallback</a>



<a href="/windows/desktop/api/mi/ne-mi-mi_cancellationreason">MI_CancellationReason</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a>