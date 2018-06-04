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

# RoUnregisterForApartmentShutdown function


## -description


Unregisters a previously registered <a href="https://msdn.microsoft.com/28EDAC77-5175-4AF7-A06C-B735336AAD9B">IApartmentShutdown</a> interface.


## -parameters




### -param regCookie [in]

A registration cookie obtained from a previous call to the <a href="https://msdn.microsoft.com/DE0C79AD-D80F-44EE-A628-147FC8474905">RoRegisterForApartmentShutdown</a> function.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call the <b>RoUnregisterForApartmentShutdown</b> to stop receiving apartment shutdown notifications and unregister a previously registered <a href="https://msdn.microsoft.com/28EDAC77-5175-4AF7-A06C-B735336AAD9B">IApartmentShutdown</a> interface.

<div class="alert"><b>Warning</b>  </div>
<div> </div>
Don't call the <b>RoUnregisterForApartmentShutdown</b> function from the <a href="https://msdn.microsoft.com/FAEBC952-EDCB-4855-AB2B-193B87E3ECF7">OnUninitialize</a> callback.




## -see-also




<a href="https://msdn.microsoft.com/28EDAC77-5175-4AF7-A06C-B735336AAD9B">IApartmentShutdown</a>



<a href="https://msdn.microsoft.com/DE0C79AD-D80F-44EE-A628-147FC8474905">RoRegisterForApartmentShutdown</a>
 

 

