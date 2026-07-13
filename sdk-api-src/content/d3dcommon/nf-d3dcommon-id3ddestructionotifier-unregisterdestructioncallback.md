---
UID: NF:d3dcommon.ID3DDestructionNotifier.UnregisterDestructionCallback
title: ID3DDestructionNotifier::UnregisterDestructionCallback (d3dcommon.h)
description: Unregisters a callback that was registered with [RegisterDestructionCallback](/windows/win32/api/d3dcommon/nf-d3dcommon-id3ddestructionotifier-registerdestructioncallback).
helpviewer_keywords: ["ID3DDestructionNotifier interface [Direct3D]","UnregisterDestructionCallback method","ID3DDestructionNotifier.UnregisterDestructionCallback","ID3DDestructionNotifier::UnregisterDestructionCallback","UnregisterDestructionCallback","UnregisterDestructionCallback method [Direct3D]","UnregisterDestructionCallback method [Direct3D]","ID3DDestructionNotifier interface","d3dcommon/ID3DDestructionNotifier::UnregisterDestructionCallback","direct3d11.id3ddestructionnotifier_unregisterdestructioncallback"]
tech.root: direct3d11
ms.date: 10/06/2020
ms.keywords: ID3DDestructionNotifier interface [Direct3D],UnregisterDestructionCallback method, ID3DDestructionNotifier.UnregisterDestructionCallback, ID3DDestructionNotifier::UnregisterDestructionCallback, UnregisterDestructionCallback, UnregisterDestructionCallback method [Direct3D], UnregisterDestructionCallback method [Direct3D],ID3DDestructionNotifier interface, d3dcommon/ID3DDestructionNotifier::UnregisterDestructionCallback, direct3d11.id3ddestructionnotifier_unregisterdestructioncallback
req.header: d3dcommon.h
req.include-header: 
req.target-type: Windows
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
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - ID3DDestructionNotifier::UnregisterDestructionCallback
 - d3dcommon/ID3DDestructionNotifier::UnregisterDestructionCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3dcommon.h
api_name:
 - ID3DDestructionNotifier.UnregisterDestructionCallback
---

## -description

Unregisters a callback that was registered with [RegisterDestructionCallback](/windows/win32/api/d3dcommon/nf-d3dcommon-id3ddestructionotifier-registerdestructioncallback).

## -parameters

### -param callbackID

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

The **UINT** that was created by the *pCallbackID* argument to <b><a href="/windows/win32/api/d3dcommon/nf-d3dcommon-id3ddestructionotifier-registerdestructioncallback">ID3DDestructionNotifier::RegisterDestructionCallback</a></b>.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If this function succeeds, it returns **S_OK**.

## -see-also

<a href="/windows/win32/api/d3dcommon/nn-d3dcommon-id3ddestructionotifier">ID3DDestructionNotifier</a>

<a href="/windows/win32/api/d3dcommon/nf-d3dcommon-id3ddestructionotifier-registerdestructioncallback">ID3DDestructionNotifier::RegisterDestructionCallback</a>
