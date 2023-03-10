---
UID: NF:roerrorapi.RoInspectCapturedStackBackTrace
title: RoInspectCapturedStackBackTrace function
description: Provides a way to for debuggers to inspect a call stack from a target process.
helpviewer_keywords: ["RoInspectCapturedStackBackTrace","RoInspectCapturedStackBackTrace function [Windows Runtime]","roerrorapi/RoInspectCapturedStackBackTrace","winrt.roinspectcapturedstackbacktrace"]
old-location: winrt\roinspectcapturedstackbacktrace.htm
tech.root: WinRT
ms.assetid: 2C5B04DD-888B-4400-A01D-CDF9DD870584
ms.date: 12/5/2018
ms.keywords: RoInspectCapturedStackBackTrace, RoInspectCapturedStackBackTrace function [Windows Runtime], roerrorapi/RoInspectCapturedStackBackTrace, winrt.roinspectcapturedstackbacktrace
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - RoInspectCapturedStackBackTrace
 - roerrorapi/RoInspectCapturedStackBackTrace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
 - RoInspectCapturedStackBackTrace
---

# RoInspectCapturedStackBackTrace function


## -description

Provides a way to for debuggers to inspect a call stack from a target process.

## -parameters

### -param targetErrorInfoAddress [in]

The address of the error info object in the target process. Get the <i>targetErrorInfoAddress</i> by calling the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roinspectthreaderrorinfo">RoInspectThreadErrorInfo</a> function.

### -param machine

The machine to debug.

### -param readMemoryCallback

A callback function to read the buffer from the target TEB address space.

### -param context [in, optional]

Custom context data.

### -param frameCount [out]

The number of stack frames stored in the error object.

### -param targetBackTraceAddress [out]

The stack back trace address in the target process.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>RoInspectCapturedStackBackTrace</b> function takes a pointer to a system error object  and fills <i>frameCount</i> with the number of stack frames stored in the error object,  and it fills <i>targetBackTraceAddress</i> with the stack back trace address in the target process. The <b>RoInspectCapturedStackBackTrace</b> function tries to confirm that <i>targetErrorInfoAddress</i> points is to a system error object and fails if it can't match the version signature.

Get the <i>targetErrorInfoAddress</i> by calling the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roinspectthreaderrorinfo">RoInspectThreadErrorInfo</a> function.

## -see-also

<a href="/windows/desktop/api/roerrorapi/nc-roerrorapi-pinspect_memory_callback">PINSPECT_MEMORY_CALLBACK</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roinspectthreaderrorinfo">RoInspectThreadErrorInfo</a>