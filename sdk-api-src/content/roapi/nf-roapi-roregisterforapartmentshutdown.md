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

# RoRegisterForApartmentShutdown function


## -description


Registers an <a href="https://msdn.microsoft.com/28EDAC77-5175-4AF7-A06C-B735336AAD9B">IApartmentShutdown</a> callback to be invoked when the current apartment shuts down.


## -parameters




### -param callbackObject [in]

The application-supplied <a href="https://msdn.microsoft.com/28EDAC77-5175-4AF7-A06C-B735336AAD9B">IApartmentShutdown</a> interface. 


### -param apartmentIdentifier [out]

The identifier for the current apartment.


### -param regCookie

TBD




#### - pRegCookie [out]

A cookie that you can use to unregister the callback.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To receive apartment shutdown notifications, your app must register its apartment shutdown handler with the system by calling the <b>RoRegisterForApartmentShutdown</b> function.

<div class="alert"><b>Warning</b>  </div>
<div> </div>
Don't call the <b>RoRegisterForApartmentShutdown</b> function from the <a href="https://msdn.microsoft.com/FAEBC952-EDCB-4855-AB2B-193B87E3ECF7">OnUninitialize</a> callback.




## -see-also




<a href="https://msdn.microsoft.com/28EDAC77-5175-4AF7-A06C-B735336AAD9B">IApartmentShutdown</a>



<a href="https://msdn.microsoft.com/B6E22C50-14EC-4B0F-8C97-7D1062BF6072">RoUnregisterForApartmentShutdown</a>
 

 

