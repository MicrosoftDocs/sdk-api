---
UID: NF:winbase.GetXStateFeaturesMask
title: GetXStateFeaturesMask function (winbase.h)
author: windows-sdk-content
description: Returns the mask of XState features set within a CONTEXT structure.
old-location: base\getxstatefeaturesmask.htm
tech.root: Debug
ms.assetid: D9A8D0B6-21E3-46B7-AB88-CE2FF4025A17
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetXStateFeaturesMask, GetXStateFeaturesMask function, base.getxstatefeaturesmask, winbase/GetXStateFeaturesMask
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
 - GetXStateFeaturesMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetXStateFeaturesMask function


## -description


Returns the mask of XState features set within a 
    <a href="https://msdn.microsoft.com/b27205a2-2c33-4f45-8948-9919bcd2355a">CONTEXT</a> structure.


## -parameters




### -param Context [in]

A pointer to a <a href="https://msdn.microsoft.com/b27205a2-2c33-4f45-8948-9919bcd2355a">CONTEXT</a> structure that has been 
      initialized with <a href="https://msdn.microsoft.com/909BF5F7-0622-4B22-A2EC-27722389700A">InitializeContext</a>.


### -param FeatureMask [out]

A pointer to a variable that receives the mask of XState features which are present in the specified 
      <b>CONTEXT</b> structure.


## -returns



This function returns <b>TRUE</b> if successful, otherwise 
      <b>FALSE</b>.




## -remarks



The <b>GetXStateFeaturesMask</b> function returns 
     the mask of valid features in the specified context.  If a 
     <a href="https://msdn.microsoft.com/b27205a2-2c33-4f45-8948-9919bcd2355a">CONTEXT</a> is to be passed to 
     <a href="https://msdn.microsoft.com/3b65283e-34d2-4374-87fe-fa8ae45fbbcf">GetThreadContext</a> or 
     <a href="https://msdn.microsoft.com/1bac28e1-3558-43c4-97e4-d8bb9514c38e">Wow64GetThreadContext</a>, the application must 
     call <a href="https://msdn.microsoft.com/64ADEA8A-DE78-437E-AE68-A68E7214C5FD">SetXStateFeaturesMask</a> to set which 
     features are to be retrieved. 
     <b>GetXStateFeaturesMask</b> should then be called on 
     the <b>CONTEXT</b> returned by 
     <b>GetThreadContext</b> or 
     <b>Wow64GetThreadContext</b> to determine which 
     feature areas contain valid data. If a particular feature bit is not set, the corresponding state is in a 
     processor-specific <b>INITIALIZED</b> state and the contents of the feature area retrieved by 
     <a href="https://msdn.microsoft.com/7AAEA13B-E4A4-4410-BFC7-09B81B92FF26">LocateXStateFeature</a> are undefined.

The definition of XState features are processor vendor specific. Please refer to the relevant processor 
     reference manuals for additional information on a particular feature.


<div class="alert"><b>Note</b>  The value returned by 
      <b>GetXStateFeaturesMask</b> on a 
      <a href="https://msdn.microsoft.com/b27205a2-2c33-4f45-8948-9919bcd2355a">CONTEXT</a> after a context operation will always be a subset 
      of the mask specified in a call to 
      <a href="https://msdn.microsoft.com/64ADEA8A-DE78-437E-AE68-A68E7214C5FD">SetXStateFeaturesMask</a> prior to the context 
      operation.</div>
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




<a href="https://msdn.microsoft.com/b27205a2-2c33-4f45-8948-9919bcd2355a">CONTEXT</a>



<a href="https://msdn.microsoft.com/3b65283e-34d2-4374-87fe-fa8ae45fbbcf">GetThreadContext</a>



<a href="https://msdn.microsoft.com/76357e08-a53c-4490-b08d-1c26900a3826">Intel AVX</a>



<a href="https://msdn.microsoft.com/64ADEA8A-DE78-437E-AE68-A68E7214C5FD">SetXStateFeaturesMask</a>



<a href="https://msdn.microsoft.com/F7937402-1173-4647-B9FF-856C0925C1C3">Working with XState Context</a>



<a href="https://msdn.microsoft.com/1bac28e1-3558-43c4-97e4-d8bb9514c38e">Wow64GetThreadContext</a>
 

 

