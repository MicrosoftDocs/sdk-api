---
UID: NF:winbase.GetEnabledXStateFeatures
title: GetEnabledXStateFeatures function
author: windows-sdk-content
description: Gets a mask of enabled XState features on x86 or x64 processors.
old-location: base\getenabledxstatefeatures.htm
old-project: Debug
ms.assetid: E7DE090F-F83E-440D-B2A3-BCF160889F2E
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetEnabledXStateFeatures, GetEnabledXStateFeatures function, base.getenabledxstatefeatures, winbase/GetEnabledXStateFeatures
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
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
 - GetEnabledXStateFeatures
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetEnabledXStateFeatures function


## -description


Gets a mask of enabled XState features on x86 or x64 processors.

The definition of XState feature bits are processor vendor specific. Please refer to the relevant processor 
    reference manuals for additional information on a particular feature.


## -parameters






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



<b>Windows 7 with SP1 and Windows Server 2008 R2 with SP1:  </b>The <a href="https://msdn.microsoft.com/76357e08-a53c-4490-b08d-1c26900a3826">AVX API</a> is first implemented on 
       Windows 7 with SP1 and Windows Server 2008 R2 with SP1 . Since there is no SDK for SP1, that means there are 
       no available headers and library files to work with. In this situation, a caller must declare the needed 
       functions from this documentation and get pointers to them using 
       <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> on 
       "Kernel32.dll", followed by calls to 
       <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>. See 
       <a href="https://msdn.microsoft.com/F7937402-1173-4647-B9FF-856C0925C1C3">Working with XState Context</a> for 
       details.






## -see-also




<a href="https://msdn.microsoft.com/76357e08-a53c-4490-b08d-1c26900a3826">Intel AVX</a>



<a href="https://msdn.microsoft.com/F7937402-1173-4647-B9FF-856C0925C1C3">Working with XState Context</a>
 

 

