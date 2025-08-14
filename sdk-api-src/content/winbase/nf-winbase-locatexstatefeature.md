---
UID: NF:winbase.LocateXStateFeature
title: LocateXStateFeature function (winbase.h)
description: Retrieves a pointer to the processor state for an XState feature within a CONTEXT structure.
helpviewer_keywords: ["LocateXStateFeature","LocateXStateFeature function","base.locatexstatefeature","winbase/LocateXStateFeature"]
old-location: base\locatexstatefeature.htm
tech.root: Debug
ms.assetid: 7AAEA13B-E4A4-4410-BFC7-09B81B92FF26
ms.date: 12/05/2018
ms.keywords: LocateXStateFeature, LocateXStateFeature function, base.locatexstatefeature, winbase/LocateXStateFeature
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 with SP1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LocateXStateFeature
 - winbase/LocateXStateFeature
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-xstate-l2-1-2.dll
 - api-ms-win-core-xstate-l2-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-Xstate-l2-1-0.dll
 - KernelBase.dll
api_name:
 - LocateXStateFeature
---

# LocateXStateFeature function


## -description

Retrieves a pointer to the processor state for an XState feature within a 
    <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure.

The definition of XState feature bits are processor vendor specific. Please refer to the relevant processor 
    reference manuals for additional information on a particular feature.

## -parameters

### -param Context [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure containing the state 
      to retrieve or set. This <b>CONTEXT</b> should have been 
      initialized with <a href="/windows/desktop/api/winbase/nf-winbase-initializecontext">InitializeContext</a> with the 
      <b>CONTEXT_XSTATE</b> flag set in the <i>ContextFlags</i> 
      parameter.

### -param FeatureId [in]

The number of the feature to locate within the 
      <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure.

### -param Length [out, optional]

A pointer to a variable which receives the length of the feature area in bytes. The contents of this 
      variable are undefined if this function returns <b>NULL</b>.

## -returns

If the specified feature is supported by the system and the specified 
       <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure has been initialized with the 
       <b>CONTEXT_XSTATE</b> flag, this function returns a pointer to the feature area for the 
       specified feature.  The contents and layout of this area is processor-specific.

If the <b>CONTEXT_XSTATE</b> flag is not set in the 
       <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure or the 
       <i>FeatureID</i> is not supported by the system, the return value is 
       <b>NULL</b>. No additional error information is available.

## -remarks

The <b>LocateXStateFeature</b> function must be used 
    to find an individual XState feature within an extensible 
    <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure. Features are not necessarily contiguous 
    in memory and applications should not assume the offset between two consecutive features will remain constant in 
    the future.

The <i>FeatureID</i> parameter of the function corresponds to a bit within the feature 
    mask. For example, <i>FeatureId</i> 2 corresponds to a <i>FeatureMask</i> of 
    4 in <a href="/windows/desktop/api/winbase/nf-winbase-setxstatefeaturesmask">SetXStateFeaturesMask</a>. 
    <i>FeatureID</i> values of 0 and 1 correspond to X87 FPU state and SSE state, 
    respectively.

If you are setting XState on a thread via the 
    <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a> or 
    <a href="/windows/win32/api/wow64apiset/">Wow64SetThreadContext</a> 
    APIs, you must also call 
    <a href="/windows/desktop/api/winbase/nf-winbase-setxstatefeaturesmask">SetXStateFeaturesMask</a> on the 
    <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure with the mask value of the filled-in 
    feature to mark the feature as active.


<b>Windows 7 with SP1 and Windows Server 2008 R2 with SP1:  </b>The <a href="/windows/desktop/Debug/avx-support-portal">AVX API</a> is first implemented on 
       Windows 7 with SP1 and Windows Server 2008 R2 with SP1 . Since there is no SDK for SP1, that means there are 
       no available headers and library files to work with. In this situation, a caller must declare the needed 
       functions from this documentation and get pointers to them using 
       <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a> on 
       "Kernel32.dll", followed by calls to 
       <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>. See 
       <a href="/windows/desktop/Debug/working-with-xstate-context">Working with XState Context</a> for 
       details.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a>



<a href="/windows/desktop/Debug/avx-support-portal">Intel AVX</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setxstatefeaturesmask">SetXStateFeaturesMask</a>



<a href="/windows/desktop/Debug/working-with-xstate-context">Working with XState Context</a>



<a href="/windows/win32/api/wow64apiset/">Wow64SetThreadContext</a>