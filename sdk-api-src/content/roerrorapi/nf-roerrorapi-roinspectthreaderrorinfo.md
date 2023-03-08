---
UID: NF:roerrorapi.RoInspectThreadErrorInfo
title: RoInspectThreadErrorInfo function
description: Gets the error object that represents the call stack at the point where the error originated.
helpviewer_keywords: ["RoInspectThreadErrorInfo","RoInspectThreadErrorInfo function [Windows Runtime]","roerrorapi/RoInspectThreadErrorInfo","winrt.roinspectthreaderrorinfo"]
old-location: winrt\roinspectthreaderrorinfo.htm
tech.root: WinRT
ms.assetid: DE7A930A-89CD-45C0-A232-800E5A5648F8
ms.date: 12/5/2018
ms.keywords: RoInspectThreadErrorInfo, RoInspectThreadErrorInfo function [Windows Runtime], roerrorapi/RoInspectThreadErrorInfo, winrt.roinspectthreaderrorinfo
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
 - RoInspectThreadErrorInfo
 - roerrorapi/RoInspectThreadErrorInfo
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
 - RoInspectThreadErrorInfo
---

# RoInspectThreadErrorInfo function


## -description

Gets the error object that represents the call stack at the point where the error originated

## -parameters

### -param targetTebAddress [in]

The target thread environment block (TEB).

### -param machine

The machine to debug.

### -param readMemoryCallback

A callback function to read the buffer from the target TEB address space.

### -param context [in, optional]

Custom context data.

### -param targetErrorInfoAddress [out]

The address of the error object.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the call to <b>RoInspectThreadErrorInfo</b> is  successful, <i>targetErrorInfoAddress</i> contains the address of an error object that you can pass to the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace">RoInspectCapturedStackBackTrace</a> function to get the call stack at the point where the error was originated.

## -see-also

<a href="/windows/desktop/api/roerrorapi/nc-roerrorapi-pinspect_memory_callback">PINSPECT_MEMORY_CALLBACK</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace">RoInspectCapturedStackBackTrace</a>