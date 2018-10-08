---
UID: NF:winbase.SetXStateFeaturesMask
title: SetXStateFeaturesMask function
author: windows-sdk-content
description: Sets the mask of XState features set within a CONTEXT structure.
old-location: base\setxstatefeaturesmask.htm
tech.root: debug
ms.assetid: 64ADEA8A-DE78-437E-AE68-A68E7214C5FD
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: SetXStateFeaturesMask, SetXStateFeaturesMask function, base.setxstatefeaturesmask, winbase/SetXStateFeaturesMask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetXStateFeaturesMask function


## -description


Sets the mask of XState features set within a 
    <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure.


## -parameters




### -param Context [in, out]

A pointer to a <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure that has been 
      initialized with <a href="https://msdn.microsoft.com/909BF5F7-0622-4B22-A2EC-27722389700A">InitializeContext</a>.


### -param FeatureMask [in]

A mask of XState features to set in the specified 
      <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure.


## -returns



This function returns <b>TRUE</b> if successful, otherwise 
      <b>FALSE</b>.




## -remarks



The <b>SetXStateFeaturesMask</b> function sets the 
     mask of valid features in the specified context. Before calling 
     <a href="https://msdn.microsoft.com/3b65283e-34d2-4374-87fe-fa8ae45fbbcf">GetThreadContext</a>, 
     <a href="https://msdn.microsoft.com/1bac28e1-3558-43c4-97e4-d8bb9514c38e">Wow64GetThreadContext</a>, 
     <a href="https://msdn.microsoft.com/be134953-b569-48ea-80ac-ab14dee24500">SetThreadContext</a>, or 
     <a href="https://msdn.microsoft.com/4119c945-b654-4634-a88b-e41bc762018a">Wow64SetThreadContext</a> the application must call 
     <b>SetXStateFeaturesMask</b> to specify which set of 
     features to retrieve or set.  The system silently ignores any feature specified in the 
     <i>FeatureMask</i> which is not enabled on the processor.


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



<a href="https://msdn.microsoft.com/3b65283e-34d2-4374-87fe-fa8ae45fbbcf">GetThreadContext</a>



<a href="https://msdn.microsoft.com/76357e08-a53c-4490-b08d-1c26900a3826">Intel AVX</a>



<a href="https://msdn.microsoft.com/be134953-b569-48ea-80ac-ab14dee24500">SetThreadContext</a>



<a href="https://msdn.microsoft.com/F7937402-1173-4647-B9FF-856C0925C1C3">Working with XState Context</a>



<a href="https://msdn.microsoft.com/1bac28e1-3558-43c4-97e4-d8bb9514c38e">Wow64GetThreadContext</a>



<a href="https://msdn.microsoft.com/4119c945-b654-4634-a88b-e41bc762018a">Wow64SetThreadContext</a>
 

 

