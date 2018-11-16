---
UID: NC:werapi.PFN_WER_RUNTIME_EXCEPTION_EVENT
title: PFN_WER_RUNTIME_EXCEPTION_EVENT
author: windows-sdk-content
description: WER calls this function to determine whether the exception handler is claiming the crash.
old-location: wer\outofprocessexceptioneventcallback.htm
tech.root: wer
ms.assetid: 22033278-2be3-4621-b618-3ccd21fb4cdd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: OutOfProcessExceptionEventCallback, OutOfProcessExceptionEventCallback callback function [Windows Error Reporting], PFN_WER_RUNTIME_EXCEPTION_EVENT, PFN_WER_RUNTIME_EXCEPTION_EVENT callback, wer.outofprocessexceptioneventcallback, werapi/OutOfProcessExceptionEventCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Werapi.h
api_name:
 - OutOfProcessExceptionEventCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_WER_RUNTIME_EXCEPTION_EVENT callback function


## -description


 WER calls this function to determine whether the exception handler is claiming the crash.

The <b>PFN_WER_RUNTIME_EXCEPTION_EVENT</b> type defines a pointer to this callback function. You must use "OutOfProcessExceptionEventCallback" as the name of the callback function.


## -parameters




### -param pContext [in]

A pointer to arbitrary context information that you specified when you called the <a href="https://msdn.microsoft.com/b0fb2c0d-cc98-43cc-a508-e80545377b7f">WerRegisterRuntimeExceptionModule</a> function to register the exception handler.


### -param pExceptionInformation [in]

A <a href="https://msdn.microsoft.com/fcf956ac-6015-439c-aec6-8f6a826ff269">WER_RUNTIME_EXCEPTION_INFORMATION</a> structure that contains the exception information. Use the information to determine whether you want to claim the crash.


### -param *pbOwnershipClaimed [out]

Set to <b>TRUE</b> if the exception handler is claiming this crash; otherwise, <b>FALSE</b>. If you set this parameter to <b>FALSE</b>, do not set the rest of the out parameters.


### -param pwszEventName [out]

A caller-allocated buffer that you use to specify the event name used to identify this crash.


### -param pchSize [in, out]

The size, in characters, of the <i>pwszEventName</i> buffer. The buffer is limited to MAX_PATH characters. The size includes the null-terminating character.


### -param pdwSignatureCount [out]

The number of report parameters that you will provide. The valid range of values is one to 10. If you specify a value greater than 10, WER will ignore the value and collect only the first 10 parameters. If you specify zero, the reporting process will be indeterminate.

This value determines the number of times that WER calls your <a href="https://msdn.microsoft.com/892498db-0265-4276-9735-63a8104ecaa9">OutOfProcessExceptionEventSignatureCallback</a> function.


## -returns



Return <b>S_OK</b>, even if the exception handler is not claiming this crash. If you return other failure codes, WER reverts to its default crash reporting behavior if no other handlers are registered.




## -remarks



You must implement this function in your exception handler DLL.




## -see-also




<a href="https://msdn.microsoft.com/b0fb2c0d-cc98-43cc-a508-e80545377b7f">WerRegisterRuntimeExceptionModule</a>
 

 

