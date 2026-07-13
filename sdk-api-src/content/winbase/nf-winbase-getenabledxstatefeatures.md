---
UID: NF:winbase.GetEnabledXStateFeatures
title: GetEnabledXStateFeatures function (winbase.h)
description: Gets a mask of enabled XState features on x86 or x64 processors.
helpviewer_keywords: ["GetEnabledXStateFeatures","GetEnabledXStateFeatures function","base.getenabledxstatefeatures","winbase/GetEnabledXStateFeatures"]
old-location: base\getenabledxstatefeatures.htm
tech.root: Debug
ms.assetid: E7DE090F-F83E-440D-B2A3-BCF160889F2E
ms.date: 12/05/2018
ms.keywords: GetEnabledXStateFeatures, GetEnabledXStateFeatures function, base.getenabledxstatefeatures, winbase/GetEnabledXStateFeatures
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
 - GetEnabledXStateFeatures
 - winbase/GetEnabledXStateFeatures
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
 - GetEnabledXStateFeatures
---

# GetEnabledXStateFeatures function


## -description

Gets a mask of enabled XState features on x86 or x64 processors.

The definition of XState feature bits are processor vendor specific. Please refer to the relevant processor 
    reference manuals for additional information on a particular feature.



## -returns

This function returns a bitmask in which each bit represents an XState feature that is enabled on the 
      system.

## -remarks

An application should call this function to determine what features are present and enabled on the system 
     before using an XState processor feature or attempting to manipulate XState contexts. Bits 0 and 1 refer to the 
     X87 FPU and the presence of SSE registers, respectively. The meanings of specific feature bits beyond 0 and 1 are 
     defined in the Programmer Reference Manuals released by the processor vendors.
     <div class="alert"><b>Note</b>  Not all features supported by a processor may be enabled on the system. Using a feature which is not 
      enabled may result in exceptions or undefined behavior.</div>
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

<a href="/windows/desktop/Debug/avx-support-portal">Intel AVX</a>



<a href="/windows/desktop/Debug/working-with-xstate-context">Working with XState Context</a>
