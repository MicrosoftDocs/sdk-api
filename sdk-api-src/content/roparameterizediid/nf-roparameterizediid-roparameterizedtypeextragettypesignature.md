---
UID: NF:roparameterizediid.RoParameterizedTypeExtraGetTypeSignature
title: RoParameterizedTypeExtraGetTypeSignature function
author: windows-sdk-content
description: Gets the type signature used to compute the IID from the last call to RoGetParameterizedTypeInstanceIID with the specified handle.
old-location: winrt\roparameterizedtypeextragettypesignature.htm
old-project: WinRT
ms.assetid: E51A7A3D-F4BF-44BD-ACF2-B0AC7A4161EA
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: RoParameterizedTypeExtraGetTypeSignature, RoParameterizedTypeExtraGetTypeSignature function [Windows Runtime], roparameterizediid/RoParameterizedTypeExtraGetTypeSignature, winrt.roparameterizedtypeextragettypesignature
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: roparameterizediid.h
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
tech.root: 
req.typenames: RO_ERROR_REPORTING_FLAGS
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
product: Windows
targetos: Windows
req.lib: Runtimeobject.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# RoParameterizedTypeExtraGetTypeSignature function


## -description


Gets the type signature used to compute the IID from the last call to <a href="https://msdn.microsoft.com/DE908C82-5D7C-415C-B08B-31786589979B">RoGetParameterizedTypeInstanceIID</a> with the specified handle.


## -parameters




### -param extra [in]

Type: <b>ROPARAMIIDHANDLE</b>

A handle to the IID.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



