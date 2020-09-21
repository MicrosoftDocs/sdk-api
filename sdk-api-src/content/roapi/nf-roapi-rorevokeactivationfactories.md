---
UID: NF:roapi.RoRevokeActivationFactories
title: RoRevokeActivationFactories function (roapi.h)
description: Removes an array of registered activation factories from the Windows Runtime.
helpviewer_keywords: ["RoRevokeActivationFactories","RoRevokeActivationFactories function [Windows Runtime]","WinRTRevokeActivationFactories","roapi/RoRevokeActivationFactories","roapi/WinRTRevokeActivationFactories","winrt.rorevokeactivationfactories","winrt.winrtrevokeactivationfactories"]
old-location: winrt\rorevokeactivationfactories.htm
tech.root: WinRT
ms.assetid: 0311bd92-3b12-46bc-a21d-13bd57a2c545
ms.date: 12/05/2018
ms.keywords: RoRevokeActivationFactories, RoRevokeActivationFactories function [Windows Runtime], WinRTRevokeActivationFactories, roapi/RoRevokeActivationFactories, roapi/WinRTRevokeActivationFactories, winrt.rorevokeactivationfactories, winrt.winrtrevokeactivationfactories
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
 - RoRevokeActivationFactories
 - roapi/RoRevokeActivationFactories
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
 - RoRevokeActivationFactories
 - WinRTRevokeActivationFactories
---

# RoRevokeActivationFactories function


## -description

Removes an array of registered activation factories from the Windows Runtime.

## -parameters

### -param cookie [in]

Type: <b><a href="/windows/desktop/WinRT/ro-registration-cookie">RO_REGISTRATION_COOKIE</a></b>

## -remarks

Call the <b>RoRevokeActivationFactories</b> function remove the activation factories represented in the  <i>cookie</i> array from the Windows Runtime.

## -see-also

<a href="/windows/desktop/WinRT/ro-registration-cookie">RO_REGISTRATION_COOKIE</a>



<a href="/windows/desktop/api/roapi/nf-roapi-roinitialize">RoInitialize</a>



<a href="/windows/desktop/api/roapi/nf-roapi-roregisteractivationfactories">RoRegisterActivationFactories</a>