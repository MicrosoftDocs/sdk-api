---
UID: NC:werapi.PFN_WER_RUNTIME_EXCEPTION_DEBUGGER_LAUNCH
title: PFN_WER_RUNTIME_EXCEPTION_DEBUGGER_LAUNCH (werapi.h)
description: WER calls this function to let you customize the debugger launch options and launch string.
helpviewer_keywords: ["OutOfProcessExceptionEventDebuggerLaunchCallback","OutOfProcessExceptionEventDebuggerLaunchCallback callback function [Windows Error Reporting]","PFN_WER_RUNTIME_EXCEPTION_DEBUGGER_LAUNCH","PFN_WER_RUNTIME_EXCEPTION_DEBUGGER_LAUNCH callback","wer.outofprocessexceptioneventdebuggerlaunchcallback","werapi/OutOfProcessExceptionEventDebuggerLaunchCallback"]
old-location: wer\outofprocessexceptioneventdebuggerlaunchcallback.htm
tech.root: wer
ms.assetid: ecf36951-cdb5-425d-a9b1-83b7ce8aebc4
ms.date: 12/05/2018
ms.keywords: OutOfProcessExceptionEventDebuggerLaunchCallback, OutOfProcessExceptionEventDebuggerLaunchCallback callback function [Windows Error Reporting], PFN_WER_RUNTIME_EXCEPTION_DEBUGGER_LAUNCH, PFN_WER_RUNTIME_EXCEPTION_DEBUGGER_LAUNCH callback, wer.outofprocessexceptioneventdebuggerlaunchcallback, werapi/OutOfProcessExceptionEventDebuggerLaunchCallback
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
 - PFN_WER_RUNTIME_EXCEPTION_DEBUGGER_LAUNCH
 - werapi/PFN_WER_RUNTIME_EXCEPTION_DEBUGGER_LAUNCH
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
 - OutOfProcessExceptionEventDebuggerLaunchCallback
---

# PFN_WER_RUNTIME_EXCEPTION_DEBUGGER_LAUNCH callback function


## -description

 WER calls this function to let you customize the debugger launch options and launch string.

The <b>PFN_WER_RUNTIME_EXCEPTION_DEBUGGER_LAUNCH</b> type defines a pointer to this callback function. You must use "OutOfProcessExceptionEventDebuggerLaunchCallback" as the name of the callback function.

## -parameters

### -param pContext [in]

A pointer to arbitrary context information that you specified when you called the <a href="/windows/desktop/api/werapi/nf-werapi-werregisterruntimeexceptionmodule">WerRegisterRuntimeExceptionModule</a> function to register the exception handler.

### -param pExceptionInformation [in]

A <a href="/windows/desktop/api/werapi/ns-werapi-wer_runtime_exception_information">WER_RUNTIME_EXCEPTION_INFORMATION</a> structure that contains the exception information.

### -param pbIsCustomDebugger [out]

Set to <b>TRUE</b> if the custom debugger specified in the <i>pwszDebuggerLaunch</i> parameter is used to debug the crash; otherwise, set to <b>FALSE</b> to use the default debugger. If you set this parameter to  <b>FALSE</b>, do not set the <i>pwszDebuggerLaunch</i> parameter.

### -param pwszDebuggerLaunch [out]

A caller-allocated buffer that you use to specify the debugger launch string used to launch the debugger. The launch string must include the full path to the debugger and any arguments. If an argument includes multiple words, use quotes to delimit the argument. The debugger string should adhere to the same protocol as the default AeDebug debugger string (see <a href="/windows/desktop/Debug/configuring-automatic-debugging">Configuring Automatic Debugging</a>). The string must contain two formatting specifiers: %ld for the crashing process ID, and %ld for the handle to an event object to be signaled after the custom debugger has attached to the target (for a description of these specifiers, see <a href="https://msdn.microsoft.com/library/cc266343.aspx">Enabling Postmortem Debugging</a>). However, custom debuggers can choose to ignore these parameters.

### -param pchDebuggerLaunch [in, out]

The size, in characters, of the <i>pwszDebuggerLaunch</i> buffer.

### -param pbIsDebuggerAutolaunch [out]

Set to <b>TRUE</b> if you want WER to silently launch the debugger; otherwise, <b>FALSE</b> if you want WER to ask the user before launching the debugger.

## -returns

Return <b>S_OK</b>, even if no customer debugger is to be used. If you return other failure codes, WER reverts to its default crash reporting behavior.

## -remarks

You must implement this function in your exception handler DLL.

WER uses this function to determine which debugger to launch and  whether to launch the debugger automatically or ask the user before launching the debugger. Specifying a custom debugger will override the default launch string (the AeDebug registry key contains the default launch string).

WER calls this callback function only if you set the <i>pbOwnershipClaimed</i> parameter of your <a href="/windows/desktop/api/werapi/nc-werapi-pfn_wer_runtime_exception_event">OutOfProcessExceptionEventCallback</a> callback function to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/werapi/nf-werapi-werregisterruntimeexceptionmodule">WerRegisterRuntimeExceptionModule</a>