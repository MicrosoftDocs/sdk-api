---
UID: NF:winbase.GetXStateFeaturesMask
title: GetXStateFeaturesMask function (winbase.h)
description: Returns the mask of XState features set within a CONTEXT structure.
helpviewer_keywords: ["GetXStateFeaturesMask","GetXStateFeaturesMask function","base.getxstatefeaturesmask","winbase/GetXStateFeaturesMask"]
old-location: base\getxstatefeaturesmask.htm
tech.root: Debug
ms.assetid: D9A8D0B6-21E3-46B7-AB88-CE2FF4025A17
ms.date: 12/05/2018
ms.keywords: GetXStateFeaturesMask, GetXStateFeaturesMask function, base.getxstatefeaturesmask, winbase/GetXStateFeaturesMask
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
 - GetXStateFeaturesMask
 - winbase/GetXStateFeaturesMask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-xstate-l2-1-2.dll
 - Kernel32.dll
 - API-MS-Win-Core-Xstate-l2-1-0.dll
 - KernelBase.dll
 - api-ms-win-core-xstate-l2-1-1.dll
api_name:
 - GetXStateFeaturesMask
---

# GetXStateFeaturesMask function


## -description

Returns the mask of XState features set within a 
    <a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">CONTEXT</a> structure.

## -parameters

### -param Context [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">CONTEXT</a> structure that has been 
      initialized with <a href="/windows/desktop/api/winbase/nf-winbase-initializecontext">InitializeContext</a>.

### -param FeatureMask [out]

A pointer to a variable that receives the mask of XState features which are present in the specified 
      <b>CONTEXT</b> structure.

## -returns

This function returns <b>TRUE</b> if successful, otherwise 
      <b>FALSE</b>.

## -remarks

The <b>GetXStateFeaturesMask</b> function returns 
     the mask of valid features in the specified context.  If a 
     <a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">CONTEXT</a> is to be passed to 
     <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadcontext">GetThreadContext</a> or 
     <a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/winbase/nf-winbase-wow64getthreadcontext.md">Wow64GetThreadContext</a>, the application must 
     call <a href="/windows/desktop/api/winbase/nf-winbase-setxstatefeaturesmask">SetXStateFeaturesMask</a> to set which 
     features are to be retrieved. 
     <b>GetXStateFeaturesMask</b> should then be called on 
     the <b>CONTEXT</b> returned by 
     <b>GetThreadContext</b> or 
     <b>Wow64GetThreadContext</b> to determine which 
     feature areas contain valid data. If a particular feature bit is not set, the corresponding state is in a 
     processor-specific <b>INITIALIZED</b> state and the contents of the feature area retrieved by 
     <a href="/windows/desktop/api/winbase/nf-winbase-locatexstatefeature">LocateXStateFeature</a> are undefined.

The definition of XState features are processor vendor specific. Please refer to the relevant processor 
     reference manuals for additional information on a particular feature.


<div class="alert"><b>Note</b>  The value returned by 
      <b>GetXStateFeaturesMask</b> on a 
      <a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">CONTEXT</a> after a context operation will always be a subset 
      of the mask specified in a call to 
      <a href="/windows/desktop/api/winbase/nf-winbase-setxstatefeaturesmask">SetXStateFeaturesMask</a> prior to the context 
      operation.</div>
<div> </div>



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

<a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">CONTEXT</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadcontext">GetThreadContext</a>



<a href="/windows/desktop/Debug/avx-support-portal">Intel AVX</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setxstatefeaturesmask">SetXStateFeaturesMask</a>



<a href="/windows/desktop/Debug/working-with-xstate-context">Working with XState Context</a>



<a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/winbase/nf-winbase-wow64getthreadcontext.md">Wow64GetThreadContext</a>