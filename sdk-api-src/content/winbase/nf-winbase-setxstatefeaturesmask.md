---
UID: NF:winbase.SetXStateFeaturesMask
title: SetXStateFeaturesMask function (winbase.h)
description: Sets the mask of XState features set within a CONTEXT structure.
helpviewer_keywords: ["SetXStateFeaturesMask","SetXStateFeaturesMask function","base.setxstatefeaturesmask","winbase/SetXStateFeaturesMask"]
old-location: base\setxstatefeaturesmask.htm
tech.root: Debug
ms.assetid: 64ADEA8A-DE78-437E-AE68-A68E7214C5FD
ms.date: 03/15/2023
ms.keywords: SetXStateFeaturesMask, SetXStateFeaturesMask function, base.setxstatefeaturesmask, winbase/SetXStateFeaturesMask
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 with SP1 [desktop apps only]
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
 - SetXStateFeaturesMask
 - winbase/SetXStateFeaturesMask
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
 - SetXStateFeaturesMask
---

# SetXStateFeaturesMask function


## -description

Sets the mask of XState features set within a 
    <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure.

## -parameters

### -param Context [in, out]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure that has been 
      initialized with <a href="/windows/desktop/api/winbase/nf-winbase-initializecontext">InitializeContext</a>.

### -param FeatureMask [in]

A mask of XState features to set in the specified 
      <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure.

## -returns

This function returns <b>TRUE</b> if successful, otherwise 
      <b>FALSE</b>.

## -remarks

The <b>SetXStateFeaturesMask</b> function sets the 
     mask of valid features in the specified context. Before calling 
     <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadcontext">GetThreadContext</a>, 
     <a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/winbase/nf-winbase-wow64getthreadcontext.md">Wow64GetThreadContext</a>, 
     <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a>, or 
     <a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/winbase/nf-winbase-wow64setthreadcontext.md">Wow64SetThreadContext</a> the application must call 
     <b>SetXStateFeaturesMask</b> to specify which set of 
     features to retrieve or set.  The system silently ignores any feature specified in the 
     <i>FeatureMask</i> which is not enabled on the processor.


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



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadcontext">GetThreadContext</a>



<a href="/windows/desktop/Debug/avx-support-portal">Intel AVX</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a>



<a href="/windows/desktop/Debug/working-with-xstate-context">Working with XState Context</a>



<a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/winbase/nf-winbase-wow64getthreadcontext.md">Wow64GetThreadContext</a>



<a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/winbase/nf-winbase-wow64setthreadcontext.md">Wow64SetThreadContext</a>