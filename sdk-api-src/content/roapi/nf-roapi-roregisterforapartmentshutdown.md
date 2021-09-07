---
UID: NF:roapi.RoRegisterForApartmentShutdown
title: RoRegisterForApartmentShutdown function (roapi.h)
description: Registers an IApartmentShutdown callback to be invoked when the current apartment shuts down.
helpviewer_keywords: ["RoRegisterForApartmentShutdown","RoRegisterForApartmentShutdown function [Windows Runtime]","roapi/RoRegisterForApartmentShutdown","winrt.roregisterforapartmentshutdown"]
old-location: winrt\roregisterforapartmentshutdown.htm
tech.root: WinRT
ms.assetid: DE0C79AD-D80F-44EE-A628-147FC8474905
ms.date: 12/05/2018
ms.keywords: RoRegisterForApartmentShutdown, RoRegisterForApartmentShutdown function [Windows Runtime], roapi/RoRegisterForApartmentShutdown, winrt.roregisterforapartmentshutdown
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoRegisterForApartmentShutdown
 - roapi/RoRegisterForApartmentShutdown
dev_langs:
 - c++
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
---

# RoRegisterForApartmentShutdown function


## -description

Registers an <a href="/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown">IApartmentShutdown</a> callback to be invoked when the current apartment shuts down.

## -parameters

### -param callbackObject [in]

The application-supplied <a href="/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown">IApartmentShutdown</a> interface.

### -param apartmentIdentifier [out]

The identifier for the current apartment.

### -param regCookie [out]

A cookie that you can use to unregister the callback.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To receive apartment shutdown notifications, your app must register its apartment shutdown handler with the system by calling the <b>RoRegisterForApartmentShutdown</b> function.

<div class="alert"><b>Warning</b>  </div>
<div> </div>
Don't call the <b>RoRegisterForApartmentShutdown</b> function from the <a href="/windows/desktop/api/objidl/nf-objidl-iapartmentshutdown-onuninitialize">OnUninitialize</a> callback.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown">IApartmentShutdown</a>



<a href="/windows/desktop/api/roapi/nf-roapi-rounregisterforapartmentshutdown">RoUnregisterForApartmentShutdown</a>