---
UID: NF:roapi.RoRegisterForApartmentShutdown
title: RoRegisterForApartmentShutdown function
author: windows-sdk-content
description: Registers an IApartmentShutdown callback to be invoked when the current apartment shuts down.
old-location: winrt\roregisterforapartmentshutdown.htm
tech.root: WinRT
ms.assetid: DE0C79AD-D80F-44EE-A628-147FC8474905
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: RoRegisterForApartmentShutdown, RoRegisterForApartmentShutdown function [Windows Runtime], roapi/RoRegisterForApartmentShutdown, winrt.roregisterforapartmentshutdown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: roapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-l1-1-0.dll
api_name:
 - RoRegisterForApartmentShutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RoRegisterForApartmentShutdown function


## -description


Registers an <a href="https://msdn.microsoft.com/28EDAC77-5175-4AF7-A06C-B735336AAD9B">IApartmentShutdown</a> callback to be invoked when the current apartment shuts down.


## -parameters




### -param callbackObject [in]

The application-supplied <a href="https://msdn.microsoft.com/28EDAC77-5175-4AF7-A06C-B735336AAD9B">IApartmentShutdown</a> interface. 


### -param apartmentIdentifier [out]

The identifier for the current apartment.


### -param regCookie [out]

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
 

 

