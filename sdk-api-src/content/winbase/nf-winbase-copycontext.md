---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CopyContext function


## -description


Copies a source context structure (including any XState) onto an initialized destination context 
    structure.


## -parameters




### -param Destination [in, out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">CONTEXT</a> structure that receives the 
      context copied from the <i>Source</i>. The 
      <b>CONTEXT</b> structure should be initialized by calling 
      <a href="https://msdn.microsoft.com/909BF5F7-0622-4B22-A2EC-27722389700A">InitializeContext</a> before calling this 
      function.


### -param ContextFlags [in]

Flags specifying the pieces of the <i>Source</i>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">CONTEXT</a> structure that will be copied into the 
      destination. This must be a subset of the <i>ContextFlags</i> specified when calling 
      <a href="https://msdn.microsoft.com/909BF5F7-0622-4B22-A2EC-27722389700A">InitializeContext</a> on the 
      <i>Destination</i> <b>CONTEXT</b>.


### -param Source [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">CONTEXT</a> structure from which to copy 
      processor context data.


## -returns



This function returns <b>TRUE</b> if the context was copied successfully, otherwise 
      <b>FALSE</b>. To get extended error information, call 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The function copies data from the <i>Source</i>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">CONTEXT</a> over the corresponding data in the 
     <i>Destination</i> <b>CONTEXT</b>, including 
     extended context if any is present. The <i>Destination</i>
<b>CONTEXT</b> must have been initialized with 
     <a href="https://msdn.microsoft.com/909BF5F7-0622-4B22-A2EC-27722389700A">InitializeContext</a> to ensure proper alignment and 
     initialization. If any data is present in the <i>Destination</i>
<b>CONTEXT</b> and the corresponding flag is not set in the 
     <i>Source</i> <b>CONTEXT</b> or in the 
     <i>ContextFlags</i> parameter, the data remains valid in the 
     <i>Destination</i>.


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




<a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">CONTEXT</a>



<a href="https://msdn.microsoft.com/909BF5F7-0622-4B22-A2EC-27722389700A">InitializeContext</a>



<a href="https://msdn.microsoft.com/76357e08-a53c-4490-b08d-1c26900a3826">Intel AVX</a>



<a href="https://msdn.microsoft.com/F7937402-1173-4647-B9FF-856C0925C1C3">Working with XState Context</a>
 

 

