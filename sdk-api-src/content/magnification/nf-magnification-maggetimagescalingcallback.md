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

# MagGetImageScalingCallback function


## -description



<div class="alert"><b>Note</b>  The <b>MagGetImageScalingCallback</b> function is deprecated in Windows 7 and later, and should not be used in new applications.  There is no alternate functionality.</div>
<div> </div>


Retrieves the registered callback function that implements a custom transform for image scaling. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The magnification window.


## -returns



Type: <b><a href="https://msdn.microsoft.com/9452fe5d-d8e9-4953-b55b-7bf792cabe16">MagImageScalingCallback</a></b>

Returns the registered <a href="https://msdn.microsoft.com/9452fe5d-d8e9-4953-b55b-7bf792cabe16">MagImageScalingCallback</a> callback function, or <b>NULL</b> if no callback is registered.




## -remarks



This function returns <b>NULL</b> if Windows Display Driver Model (WDDM) is not supported.

This function works only when <a href="https://msdn.microsoft.com/fb1e0f1e-a6db-4961-bfa5-9c2218f8c950">Desktop Window Manager</a> (DWM) is off.




## -see-also




<a href="https://msdn.microsoft.com/9452fe5d-d8e9-4953-b55b-7bf792cabe16">MagImageScalingCallback</a>



<a href="https://msdn.microsoft.com/6985f35d-89bf-46b1-b063-fd93492b66d5">MagSetImageScalingCallback</a>
 

 

