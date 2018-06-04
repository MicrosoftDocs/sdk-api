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

# RegQueryReflectionKey function


## -description


Determines whether reflection has been disabled or enabled for the specified key.


## -parameters




### -param hBase [in]

A handle to the registry key.
      This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>, <a href="https://msdn.microsoft.com/f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2">RegCreateKeyTransacted</a>, <a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>, or 
<a href="https://msdn.microsoft.com/11663ed2-d17c-4f08-be7b-9b591271fbcd">RegOpenKeyTransacted</a> function; it cannot specify a key on a remote computer.


### -param bIsReflectionDisabled [out]

A value that indicates whether reflection has been disabled through <a href="https://msdn.microsoft.com/294a1d28-d09f-44a3-8bc0-6fae50c3a8f8">RegDisableReflectionKey</a> or enabled through <a href="https://msdn.microsoft.com/6dfbc3d8-cd71-4ee9-a10b-955c26a6894c">RegEnableReflectionKey</a>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
       <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the
       FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



On WOW64, 32-bit applications view a registry tree that is separate from the registry tree that 64-bit 
    applications view. Registry reflection copies specific registry keys and values between the two views.

To disable registry reflection, use the 
    <a href="https://msdn.microsoft.com/294a1d28-d09f-44a3-8bc0-6fae50c3a8f8">RegDisableReflectionKey</a> function. To restore 
    reflection for a disabled key, use the 
    <a href="https://msdn.microsoft.com/6dfbc3d8-cd71-4ee9-a10b-955c26a6894c">RegEnableReflectionKey</a> function.




## -see-also




<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/294a1d28-d09f-44a3-8bc0-6fae50c3a8f8">RegDisableReflectionKey</a>



<a href="https://msdn.microsoft.com/6dfbc3d8-cd71-4ee9-a10b-955c26a6894c">RegEnableReflectionKey</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/b3989f79-0439-485a-96c1-4f2227d48653">Registry Redirector</a>
 

 

