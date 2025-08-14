---
UID: NF:winbase.InitializeContext
title: InitializeContext function (winbase.h)
description: Initializes a CONTEXT structure inside a buffer with the necessary size and alignment.
helpviewer_keywords: ["InitializeContext","InitializeContext function","base.initializecontext","winbase/InitializeContext"]
old-location: base\initializecontext.htm
tech.root: Debug
ms.assetid: 909BF5F7-0622-4B22-A2EC-27722389700A
ms.date: 12/05/2018
ms.keywords: InitializeContext, InitializeContext function, base.initializecontext, winbase/InitializeContext
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
 - InitializeContext
 - winbase/InitializeContext
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
 - InitializeContext
---

# InitializeContext function


## -description

Initializes a <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure inside a buffer 
    with the necessary size and alignment.

## -parameters

### -param Buffer [out, optional]

A pointer to a buffer within which to initialize a 
      <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure. This parameter can be 
       <b>NULL</b> to determine the buffer size required to hold a context record with the 
       specified <i>ContextFlags</i>.

### -param ContextFlags [in]

A value indicating which portions of the <i>Context</i> structure should be initialized. 
      This parameter influences the size of the initialized <i>Context</i> structure.
      

<div class="alert"><b>Note</b>  <b>CONTEXT_XSTATE</b> is not part of <b>CONTEXT_FULL</b> or 
       <b>CONTEXT_ALL</b>.  It must be specified separately if an XState context is desired.</div>
<div> </div>

### -param Context [out, optional]

A pointer to a variable which receives the address of the initialized 
      <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure within the 
      <i>Buffer</i>.
      

<div class="alert"><b>Note</b>  Due to alignment requirements of <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structures, 
       the value returned in <i>Context</i> may not be at the beginning of the supplied 
       buffer.</div>
<div> </div>

### -param ContextLength [in, out]

On input, specifies the length of the buffer pointed to by <i>Buffer</i>, in bytes. If 
      the buffer is not large enough to contain the specified portions of the 
      <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a>, the function fails, 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
      <b>ERROR_INSUFFICIENT_BUFFER</b>, and <i>ContextLength</i> is set to the 
      required size of the buffer.  If the function fails with an error other than 
      <b>ERROR_INSUFFICIENT_BUFFER</b>, the contents of 
      <i>ContextLength</i> are undefined.

## -returns

This function returns <b>TRUE</b> if successful, otherwise 
      <b>FALSE</b>. To get extended error information, call 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<i>InitializeContext</i> can be used to initialize a 
    <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure within a buffer with the required size and 
    alignment characteristics.  This routine is required if the <b>CONTEXT_XSTATE</b> <i>ContextFlag</i> is specified since the required context size and alignment may change 
    depending on which processor features are enabled on the system.

First, call this function with the 
    <i>ContextFlags</i> parameter set to the maximum number of features you will be using and the 
    <i>Buffer</i> parameter to <b>NULL</b>. The function returns the required 
    buffer size in bytes in the <i>ContextLength</i> parameter. Allocate enough space for the data 
    in the <i>Buffer</i> and call the function again to initialize the 
    <i>Context</i>. Upon successful completion of this routine, the 
    <i>ContextFlags</i> member of the <i>Context</i> structure is initialized, 
    but the remaining contents of the structure are undefined. Some bits specified in the 
    <i>ContextFlags</i> parameter may not be set in 
    <i>Context</i>-&gt;<i>ContextFlags</i> if they are not supported by the 
    system. Applications may subsequently remove, but must never add, bits from the 
    <i>ContextFlags</i> member of 
    <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a>.


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



<a href="/windows/desktop/api/winbase/nf-winbase-copycontext">CopyContext</a>



<a href="/windows/desktop/Debug/avx-support-portal">Intel AVX</a>



<a href="/windows/desktop/Debug/working-with-xstate-context">Working with XState Context</a>