---
UID: NF:winbase.LocateXStateFeature
title: LocateXStateFeature function
author: windows-sdk-content
description: Retrieves a pointer to the processor state for an XState feature within a CONTEXT structure.
old-location: base\locatexstatefeature.htm
old-project: debug
ms.assetid: 7AAEA13B-E4A4-4410-BFC7-09B81B92FF26
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: LocateXStateFeature, LocateXStateFeature function, base.locatexstatefeature, winbase/LocateXStateFeature
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
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
 - LocateXStateFeature
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LocateXStateFeature function


## -description


Retrieves a pointer to the processor state for an XState feature within a 
    <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure.

The definition of XState feature bits are processor vendor specific. Please refer to the relevant processor 
    reference manuals for additional information on a particular feature.


## -parameters




### -param Context [in]

A pointer to a <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure containing the state 
      to retrieve or set. This <b>CONTEXT</b> should have been 
      initialized with <a href="https://msdn.microsoft.com/909BF5F7-0622-4B22-A2EC-27722389700A">InitializeContext</a> with the 
      <b>CONTEXT_XSTATE</b> flag set in the <i>ContextFlags</i> 
      parameter.


### -param FeatureId [in]

The number of the feature to locate within the 
      <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure.


### -param Length [out, optional]

A pointer to a variable which receives the length of the feature area in bytes. The contents of this 
      variable are undefined if this function returns <b>NULL</b>.


## -returns



If the specified feature is supported by the system and the specified 
       <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure has been initialized with the 
       <b>CONTEXT_XSTATE</b> flag, this function returns a pointer to the feature area for the 
       specified feature.  The contents and layout of this area is processor-specific.

If the <b>CONTEXT_XSTATE</b> flag is not set in the 
       <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure or the 
       <i>FeatureID</i> is not supported by the system, the return value is 
       <b>NULL</b>. No additional error information is available.




## -remarks



The <b>LocateXStateFeature</b> function must be used 
    to find an individual XState feature within an extensible 
    <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure. Features are not necessarily contiguous 
    in memory and applications should not assume the offset between two consecutive features will remain constant in 
    the future.

The <i>FeatureID</i> parameter of the function corresponds to a bit within the feature 
    mask. For example, <i>FeatureId</i> 2 corresponds to a <i>FeatureMask</i> of 
    4 in <a href="https://msdn.microsoft.com/64ADEA8A-DE78-437E-AE68-A68E7214C5FD">SetXStateFeaturesMask</a>. 
    <i>FeatureID</i> values of 0 and 1 correspond to X87 FPU state and SSE state, 
    respectively.

If you are setting XState on a thread via the 
    <a href="https://msdn.microsoft.com/be134953-b569-48ea-80ac-ab14dee24500">SetThreadContext</a> or 
    <a href="https://msdn.microsoft.com/4119c945-b654-4634-a88b-e41bc762018a">Wow64SetThreadContext</a> 
    APIs, you must also call 
    <a href="https://msdn.microsoft.com/64ADEA8A-DE78-437E-AE68-A68E7214C5FD">SetXStateFeaturesMask</a> on the 
    <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure with the mask value of the filled-in 
    feature to mark the feature as active.


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




<a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a>



<a href="https://msdn.microsoft.com/76357e08-a53c-4490-b08d-1c26900a3826">Intel AVX</a>



<a href="https://msdn.microsoft.com/be134953-b569-48ea-80ac-ab14dee24500">SetThreadContext</a>



<a href="https://msdn.microsoft.com/64ADEA8A-DE78-437E-AE68-A68E7214C5FD">SetXStateFeaturesMask</a>



<a href="https://msdn.microsoft.com/F7937402-1173-4647-B9FF-856C0925C1C3">Working with XState Context</a>



<a href="https://msdn.microsoft.com/4119c945-b654-4634-a88b-e41bc762018a">Wow64SetThreadContext</a>
 

 

