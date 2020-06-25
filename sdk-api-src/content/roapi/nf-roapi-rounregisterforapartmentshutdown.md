---
UID: NF:roapi.RoUnregisterForApartmentShutdown
title: RoUnregisterForApartmentShutdown function (roapi.h)
description: Unregisters a previously registered IApartmentShutdown interface.
helpviewer_keywords: ["RoUnregisterForApartmentShutdown","RoUnregisterForApartmentShutdown function [Windows Runtime]","roapi/RoUnregisterForApartmentShutdown","winrt.rounregisterforapartmentshutdown"]
old-location: winrt\rounregisterforapartmentshutdown.htm
tech.root: WinRT
ms.assetid: B6E22C50-14EC-4B0F-8C97-7D1062BF6072
ms.date: 12/05/2018
ms.keywords: RoUnregisterForApartmentShutdown, RoUnregisterForApartmentShutdown function [Windows Runtime], roapi/RoUnregisterForApartmentShutdown, winrt.rounregisterforapartmentshutdown
f1_keywords:
- roapi/RoUnregisterForApartmentShutdown
dev_langs:
- c++
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
- RoUnregisterForApartmentShutdown
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RoUnregisterForApartmentShutdown function


## -description


Unregisters a previously registered <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown">IApartmentShutdown</a> interface.


## -parameters




### -param regCookie [in]

A registration cookie obtained from a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-roregisterforapartmentshutdown">RoRegisterForApartmentShutdown</a> function.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call the <b>RoUnregisterForApartmentShutdown</b> to stop receiving apartment shutdown notifications and unregister a previously registered <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown">IApartmentShutdown</a> interface.

<div class="alert"><b>Warning</b>  </div>
<div> </div>
Don't call the <b>RoUnregisterForApartmentShutdown</b> function from the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iapartmentshutdown-onuninitialize">OnUninitialize</a> callback.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown">IApartmentShutdown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/roapi/nf-roapi-roregisterforapartmentshutdown">RoRegisterForApartmentShutdown</a>
 

 

