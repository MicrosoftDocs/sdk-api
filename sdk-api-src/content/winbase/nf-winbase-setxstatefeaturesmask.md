---
UID: NF:winbase.SetXStateFeaturesMask
title: SetXStateFeaturesMask function (winbase.h)
author: windows-sdk-content
description: Sets the mask of XState features set within a CONTEXT structure.
old-location: base\setxstatefeaturesmask.htm
tech.root: Debug
ms.assetid: 64ADEA8A-DE78-437E-AE68-A68E7214C5FD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetXStateFeaturesMask, SetXStateFeaturesMask function, base.setxstatefeaturesmask, winbase/SetXStateFeaturesMask
ms.topic: function
f1_keywords:
- winbase/SetXStateFeaturesMask
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Xstate-l2-1-0.dll
- KernelBase.dll
api_name:
- SetXStateFeaturesMask
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetXStateFeaturesMask function


## -description


Sets the mask of XState features set within a 
    <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure.


## -parameters




### -param Context [in, out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure that has been 
      initialized with <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-initializecontext">InitializeContext</a>.


### -param FeatureMask [in]

A mask of XState features to set in the specified 
      <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure.


## -returns



This function returns <b>TRUE</b> if successful, otherwise 
      <b>FALSE</b>.




## -remarks



The <b>SetXStateFeaturesMask</b> function sets the 
     mask of valid features in the specified context. Before calling 
     <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadcontext">GetThreadContext</a>, 
     <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-wow64getthreadcontext">Wow64GetThreadContext</a>, 
     <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a>, or 
     <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-wow64setthreadcontext">Wow64SetThreadContext</a> the application must call 
     <b>SetXStateFeaturesMask</b> to specify which set of 
     features to retrieve or set.  The system silently ignores any feature specified in the 
     <i>FeatureMask</i> which is not enabled on the processor.


<b>Windows 7 with SP1 and Windows Server 2008 R2 with SP1:  </b>The <a href="https://docs.microsoft.com/windows/desktop/Debug/avx-support-portal">AVX API</a> is first implemented on 
       Windows 7 with SP1 and Windows Server 2008 R2 with SP1 . Since there is no SDK for SP1, that means there are 
       no available headers and library files to work with. In this situation, a caller must declare the needed 
       functions from this documentation and get pointers to them using 
       <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a> on 
       "Kernel32.dll", followed by calls to 
       <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>. See 
       <a href="https://docs.microsoft.com/windows/desktop/Debug/working-with-xstate-context">Working with XState Context</a> for 
       details.






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadcontext">GetThreadContext</a>



<a href="https://docs.microsoft.com/windows/desktop/Debug/avx-support-portal">Intel AVX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a>



<a href="https://docs.microsoft.com/windows/desktop/Debug/working-with-xstate-context">Working with XState Context</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-wow64getthreadcontext">Wow64GetThreadContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-wow64setthreadcontext">Wow64SetThreadContext</a>
 

 

