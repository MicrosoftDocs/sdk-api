---
UID: NF:winbase.InitializeContext2
title: InitializeContext2
ms.date: 4/28/2020
targetos: Windows
description: Initializes a CONTEXT structure inside a buffer with the necessary size and alignment, with the option to specify an XSTATE compaction mask.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: winbase.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: kernel32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - api-ms-win-core-xstate-l2-1-2.dll
 - api-ms-win-core-xstate-l2-1-1.dll
 - winbase.h
api_name:
 - InitializeContext2
f1_keywords:
 - InitializeContext2
 - winbase/InitializeContext2
dev_langs:
 - c++
---

## -description

Initializes a <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure inside a buffer 
    with the necessary size and alignment, with the option to specify an XSTATE compaction mask.

## -parameters

### -param Buffer [out, optional]

A pointer to a buffer within which to initialize a 
      <a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure. This parameter can be 
       <b>NULL</b> to determine the buffer size required to hold a context record with the 
       specified <i>ContextFlags</i>.

### -param ContextFlags

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

### -param XStateCompactionMask

Supplies the XState compaction mask to use when allocating the <i>Context</i> structure.
This parameter is only used when <b>CONTEXT_XSTATE</b> is supplied to <i>ContextFlags</i> and the system has XState enabled in compaction mode.

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

When XState is enabled in compaction mode, specifying an <i>XStateCompactionMask</i> that contains only a subset of the enabled XState components can decrease the buffer size required to store the <i>Context</i>.
This is particularly useful if the system has many XState components enabled, but the <i>Context</i> will only be used to affect a small number of XState components.
The full set of enabled XState components can be obtained by calling <a href="/windows/win32/api/winbase/nf-winbase-getenabledxstatefeatures">GetEnabledXStateFeatures</a>.
This function copies the specified XState compaction mask into the relevant location in the XState header.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a>



<a href="/windows/desktop/api/winbase/nf-winbase-copycontext">CopyContext</a>



<a href="/windows/desktop/Debug/avx-support-portal">Intel AVX</a>



<a href="/windows/desktop/Debug/working-with-xstate-context">Working with XState Context</a>
