---
UID: NF:roparameterizediid.RoFreeParameterizedTypeExtra
title: RoFreeParameterizedTypeExtra function (roparameterizediid.h)
description: Frees the handle allocated by RoGetParameterizedTypeInstanceIID.
helpviewer_keywords: ["RoFreeParameterizedTypeExtra","RoFreeParameterizedTypeExtra function [Windows Runtime]","roparameterizediid/RoFreeParameterizedTypeExtra","winrt.rofreeparameterizedtypeextra"]
old-location: winrt\rofreeparameterizedtypeextra.htm
tech.root: WinRT
ms.assetid: A9A063F3-D6E0-4383-B9AD-EA115FC3A8FD
ms.date: 12/05/2018
ms.keywords: RoFreeParameterizedTypeExtra, RoFreeParameterizedTypeExtra function [Windows Runtime], roparameterizediid/RoFreeParameterizedTypeExtra, winrt.rofreeparameterizedtypeextra
req.header: roparameterizediid.h
req.include-header: Paraminstanceapi.h
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
 - RoFreeParameterizedTypeExtra
 - roparameterizediid/RoFreeParameterizedTypeExtra
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
 - RoFreeParameterizedTypeExtra
---

# RoFreeParameterizedTypeExtra function


## -description

Frees the handle allocated by <a href="/windows/desktop/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid">RoGetParameterizedTypeInstanceIID</a>.

## -parameters

### -param extra [in]

Type: <b>ROPARAMIIDHANDLE</b>

A handle to the IID.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.