---
UID: NF:roparameterizediid.RoParameterizedTypeExtraGetTypeSignature
title: RoParameterizedTypeExtraGetTypeSignature function (roparameterizediid.h)
description: Gets the type signature used to compute the IID from the last call to RoGetParameterizedTypeInstanceIID with the specified handle.
helpviewer_keywords: ["RoParameterizedTypeExtraGetTypeSignature","RoParameterizedTypeExtraGetTypeSignature function [Windows Runtime]","roparameterizediid/RoParameterizedTypeExtraGetTypeSignature","winrt.roparameterizedtypeextragettypesignature"]
old-location: winrt\roparameterizedtypeextragettypesignature.htm
tech.root: WinRT
ms.assetid: E51A7A3D-F4BF-44BD-ACF2-B0AC7A4161EA
ms.date: 12/05/2018
ms.keywords: RoParameterizedTypeExtraGetTypeSignature, RoParameterizedTypeExtraGetTypeSignature function [Windows Runtime], roparameterizediid/RoParameterizedTypeExtraGetTypeSignature, winrt.roparameterizedtypeextragettypesignature
req.header: roparameterizediid.h
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
req.lib: Runtimeobject.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoParameterizedTypeExtraGetTypeSignature
 - roparameterizediid/RoParameterizedTypeExtraGetTypeSignature
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - runtimeobject.lib
 - runtimeobject.dll
 - API-MS-Win-Core-WinRT-roparameterizediid-l1-1-0.dll
 - ComBase.dll
api_name:
 - RoParameterizedTypeExtraGetTypeSignature
---

# RoParameterizedTypeExtraGetTypeSignature function


## -description

Gets the type signature used to compute the IID from the last call to <a href="/windows/desktop/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid">RoGetParameterizedTypeInstanceIID</a> with the specified handle.

## -parameters

### -param extra [in]

Type: <b>ROPARAMIIDHANDLE</b>

A handle to the IID.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.