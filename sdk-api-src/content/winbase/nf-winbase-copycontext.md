---
UID: NF:winbase.CopyContext
title: CopyContext function (winbase.h)
description: Copies a source context structure (including any XState) onto an initialized destination context structure.
helpviewer_keywords: ["CopyContext","CopyContext function","base.copycontext","winbase/CopyContext"]
old-location: base\copycontext.htm
tech.root: Debug
ms.assetid: 805CD02A-53BC-487C-83F8-FE804368C770
ms.date: 12/05/2018
ms.keywords: CopyContext, CopyContext function, base.copycontext, winbase/CopyContext
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
 - CopyContext
 - winbase/CopyContext
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
 - API-MS-Win-Core-xstate-l2-1-0.dll
 - KernelBase.dll
api_name:
 - CopyContext
---

# CopyContext function


## -description

Copies a source context structure (including any XState) onto an initialized destination context 
    structure.

## -parameters

### -param Destination [in, out]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure that receives the 
      context copied from the <i>Source</i>. The 
      <b>CONTEXT</b> structure should be initialized by calling 
      <a href="/windows/desktop/api/winbase/nf-winbase-initializecontext">InitializeContext</a> before calling this 
      function.

### -param ContextFlags [in]

Flags specifying the pieces of the <i>Source</i>
<a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure that will be copied into the 
      destination. This must be a subset of the <i>ContextFlags</i> specified when calling 
      <a href="/windows/desktop/api/winbase/nf-winbase-initializecontext">InitializeContext</a> on the 
      <i>Destination</i> <b>CONTEXT</b>.

### -param Source [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure from which to copy 
      processor context data.

## -returns

This function returns <b>TRUE</b> if the context was copied successfully, otherwise 
      <b>FALSE</b>. To get extended error information, call 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The function copies data from the <i>Source</i>
<a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> over the corresponding data in the 
     <i>Destination</i> <b>CONTEXT</b>, including 
     extended context if any is present. The <i>Destination</i>
<b>CONTEXT</b> must have been initialized with 
     <a href="/windows/desktop/api/winbase/nf-winbase-initializecontext">InitializeContext</a> to ensure proper alignment and 
     initialization. If any data is present in the <i>Destination</i>
<b>CONTEXT</b> and the corresponding flag is not set in the 
     <i>Source</i> <b>CONTEXT</b> or in the 
     <i>ContextFlags</i> parameter, the data remains valid in the 
     <i>Destination</i>.


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



<a href="/windows/desktop/api/winbase/nf-winbase-initializecontext">InitializeContext</a>



<a href="/windows/desktop/Debug/avx-support-portal">Intel AVX</a>



<a href="/windows/desktop/Debug/working-with-xstate-context">Working with XState Context</a>