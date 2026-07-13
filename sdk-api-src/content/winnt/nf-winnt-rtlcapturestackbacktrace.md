---
UID: NF:winnt.RtlCaptureStackBackTrace
title: RtlCaptureStackBackTrace function (winnt.h)
description: The RtlCaptureStackBackTrace routine captures a stack back trace by walking up the stack and recording the information for each frame.
helpviewer_keywords: ["CaptureStackBackTrace","RtlCaptureStackBackTrace","RtlCaptureStackBackTrace routine [Installable File System Drivers]","ifsk.rtlcapturestackbacktrace","rtlref_c329ad74-ebb1-478d-a0d2-fd2ae2c8da2a.xml","winnt/CaptureStackBackTrace","winnt/RtlCaptureStackBackTrace"]
old-location: ifsk\rtlcapturestackbacktrace.htm
tech.root: ifsk
ms.assetid: e4ad1eac-1788-4dfe-9444-f40e0de156c4
ms.date: 12/05/2018
ms.keywords: CaptureStackBackTrace, RtlCaptureStackBackTrace, RtlCaptureStackBackTrace routine [Installable File System Drivers], ifsk.rtlcapturestackbacktrace, rtlref_c329ad74-ebb1-478d-a0d2-fd2ae2c8da2a.xml, winnt/CaptureStackBackTrace, winnt/RtlCaptureStackBackTrace
req.header: winnt.h
req.include-header: Ntifs.h, FltKernel.h
req.target-type: Universal
req.target-min-winverclnt: Available in starting with Windows XP.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib; OneCoreUAP.lib on Windows 10
req.dll: NtDll.dll (user mode); NtosKrnl.exe (kernel mode)
req.irql: <= DISPATCH_LEVEL
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlCaptureStackBackTrace
 - winnt/RtlCaptureStackBackTrace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-rtlsupport-l1-2-2.dll
 - api-ms-win-core-rtlsupport-l1-2-1.dll
 - NtDll.dll
 - NtosKrnl.exe
 - API-MS-Win-Core-RTLSupport-l1-1-0.dll
 - API-MS-Win-Core-RTLSupport-l1-2-0.dll
api_name:
 - RtlCaptureStackBackTrace
 - CaptureStackBackTrace
---

# RtlCaptureStackBackTrace function


## -description

The <b>RtlCaptureStackBackTrace</b> routine captures a stack back trace by walking up the stack and recording the information for each frame.

## -parameters

### -param FramesToSkip [in]

The number of frames to skip from the start of the back trace.

### -param FramesToCapture [in]

The number of frames to be captured.

### -param BackTrace [out]

An array of pointers captured from the current stack trace.

### -param BackTraceHash [out, optional]

An optional value that can be used to organize hash tables. If this parameter is <b>NULL</b>, no hash value is computed.

This value is calculated based on the values of the pointers returned in the <i>BackTrace</i> array. Two identical stack traces will generate identical hash values.

## -returns

The number of captured frames.

