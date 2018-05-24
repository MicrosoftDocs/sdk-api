---
UID: NF:roapi.RoUnregisterForApartmentShutdown
title: RoUnregisterForApartmentShutdown function
author: windows-driver-content
description: Unregisters a previously registered IApartmentShutdown interface.
old-location: winrt\rounregisterforapartmentshutdown.htm
old-project: WinRT
ms.assetid: B6E22C50-14EC-4B0F-8C97-7D1062BF6072
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: RoUnregisterForApartmentShutdown, RoUnregisterForApartmentShutdown function [Windows Runtime], roapi/RoUnregisterForApartmentShutdown, winrt.rounregisterforapartmentshutdown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: roapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RO_INIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ComBase.dll
-	API-MS-Win-Core-WinRT-l1-1-0.dll
api_name:
-	RoUnregisterForApartmentShutdown
product: Windows
targetos: Windows
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

