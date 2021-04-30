---
UID: NC:werapi.PFN_WER_RUNTIME_EXCEPTION_EVENT
title: PFN_WER_RUNTIME_EXCEPTION_EVENT (werapi.h)
description: WER calls this function to determine whether the exception handler is claiming the crash.
helpviewer_keywords: ["OutOfProcessExceptionEventCallback","OutOfProcessExceptionEventCallback callback function [Windows Error Reporting]","PFN_WER_RUNTIME_EXCEPTION_EVENT","PFN_WER_RUNTIME_EXCEPTION_EVENT callback","wer.outofprocessexceptioneventcallback","werapi/OutOfProcessExceptionEventCallback"]
old-location: wer\outofprocessexceptioneventcallback.htm
tech.root: wer
ms.assetid: 22033278-2be3-4621-b618-3ccd21fb4cdd
ms.date: 12/05/2018
ms.keywords: OutOfProcessExceptionEventCallback, OutOfProcessExceptionEventCallback callback function [Windows Error Reporting], PFN_WER_RUNTIME_EXCEPTION_EVENT, PFN_WER_RUNTIME_EXCEPTION_EVENT callback, wer.outofprocessexceptioneventcallback, werapi/OutOfProcessExceptionEventCallback
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - PFN_WER_RUNTIME_EXCEPTION_EVENT
 - werapi/PFN_WER_RUNTIME_EXCEPTION_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Werapi.h
api_name:
 - OutOfProcessExceptionEventCallback
---

# PFN_WER_RUNTIME_EXCEPTION_EVENT callback function


## -description

 WER calls this function to determine whether the exception handler is claiming the crash.

The <b>PFN_WER_RUNTIME_EXCEPTION_EVENT</b> type defines a pointer to this callback function. You must use "OutOfProcessExceptionEventCallback" as the name of the callback function.

## -parameters

### -param pContext [in]

A pointer to arbitrary context information that you specified when you called the <a href="/windows/desktop/api/werapi/nf-werapi-werregisterruntimeexceptionmodule">WerRegisterRuntimeExceptionModule</a> function to register the exception handler.

### -param pExceptionInformation [in]

A <a href="/windows/desktop/api/werapi/ns-werapi-wer_runtime_exception_information">WER_RUNTIME_EXCEPTION_INFORMATION</a> structure that contains the exception information. Use the information to determine whether you want to claim the crash.

### -param pbOwnershipClaimed [out]

Set to <b>TRUE</b> if the exception handler is claiming this crash; otherwise, <b>FALSE</b>. If you set this parameter to <b>FALSE</b>, do not set the rest of the out parameters.

### -param pwszEventName [out]

A caller-allocated buffer that you use to specify the event name used to identify this crash.

### -param pchSize [in, out]

The size, in characters, of the <i>pwszEventName</i> buffer. The buffer is limited to MAX_PATH characters. The size includes the null-terminating character.

### -param pdwSignatureCount [out]

The number of report parameters that you will provide. The valid range of values is one to 10. If you specify a value greater than 10, WER will ignore the value and collect only the first 10 parameters. If you specify zero, the reporting process will be indeterminate.

This value determines the number of times that WER calls your <a href="/windows/desktop/api/werapi/nc-werapi-pfn_wer_runtime_exception_event_signature">OutOfProcessExceptionEventSignatureCallback</a> function.

## -returns

Return <b>S_OK</b>, even if the exception handler is not claiming this crash. If you return other failure codes, WER reverts to its default crash reporting behavior if no other handlers are registered.

## -remarks

You must implement this function in your exception handler DLL.

## -see-also

<a href="/windows/desktop/api/werapi/nf-werapi-werregisterruntimeexceptionmodule">WerRegisterRuntimeExceptionModule</a>
