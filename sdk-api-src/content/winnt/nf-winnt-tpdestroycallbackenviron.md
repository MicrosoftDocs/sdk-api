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

# TpDestroyCallbackEnviron function


## -description


Deletes the specified callback environment. Call this function when the callback environment is no longer needed for creating new thread pool objects.


## -parameters




### -param CallbackEnviron [in]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://msdn.microsoft.com/4602CB19-D8C0-460E-A853-8DDECE643A76">TpInitializeCallbackEnviron</a> function returns this structure.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/4602CB19-D8C0-460E-A853-8DDECE643A76">TpInitializeCallbackEnviron</a>



<a href="https://msdn.microsoft.com/C4715789-0DF7-436B-881F-4360A7528246">TpSetCallbackActivationContext</a>



<a href="https://msdn.microsoft.com/B14084F5-2686-4522-8024-71A07541CFE2">TpSetCallbackCleanupGroup</a>



<a href="https://msdn.microsoft.com/425898A7-5E98-490A-912A-A409D1E2DFDE">TpSetCallbackFinalizationCallback</a>



<a href="https://msdn.microsoft.com/27E7F647-1005-4499-9787-F2CE6E8B6AFF">TpSetCallbackLongFunction</a>



<a href="https://msdn.microsoft.com/8415197A-C785-492E-9C74-2055FADDF0CD">TpSetCallbackNoActivationContext</a>



<a href="https://msdn.microsoft.com/FE2CB959-25BC-4420-A921-2A65016B25CF">TpSetCallbackPersistent</a>



<a href="https://msdn.microsoft.com/3A2DA8CA-D5F2-442A-B152-11AB28681B5B">TpSetCallbackPriority</a>



<a href="https://msdn.microsoft.com/14519064-450C-409E-AA2D-B4EF4D43C180">TpSetCallbackRaceWithDll</a>



<a href="https://msdn.microsoft.com/A1BED20A-9DB5-4B5A-B1AD-60454176AB1D">TpSetCallbackThreadpool</a>
 

 

