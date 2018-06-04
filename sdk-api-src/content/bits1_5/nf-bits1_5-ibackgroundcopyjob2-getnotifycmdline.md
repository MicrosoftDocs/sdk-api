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

# IBackgroundCopyJob2::GetNotifyCmdLine


## -description


Retrieves the program to execute when the job enters the error or transferred state.


## -parameters




### -param pProgram [out]

Null-terminated string that contains the program to execute when the job enters the error or transferred state. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>pProgram</i> when done.


### -param pParameters [out]

Null-terminated string that contains the arguments of the program in <i>pProgram</i>. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>pParameters</i> when done.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -remarks



The 
<b>GetNotifyCmdLine</b> method sets <i>pProgram</i> and <i>pParameters</i> to an empty string (L"") if the 
<a href="https://msdn.microsoft.com/61b99d01-ca0f-4a89-b7ca-77d23c21a9ad">IBackgroundCopyJob2::SetNotifyCmdLine</a> method has not been called.




## -see-also




<a href="https://msdn.microsoft.com/61b99d01-ca0f-4a89-b7ca-77d23c21a9ad">IBackgroundCopyJob2::SetNotifyCmdLine</a>
 

 

