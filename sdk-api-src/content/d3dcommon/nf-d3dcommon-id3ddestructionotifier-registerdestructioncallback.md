---
UID: NF:d3dcommon.ID3DDestructionNotifier.RegisterDestructionCallback
title: ID3DDestructionNotifier::RegisterDestructionCallback (d3dcommon.h)
description: Registers a user-defined callback to be invoked when the object this **ID3DDestructionNotifier** was created from is destroyed.
helpviewer_keywords: ["ID3DDestructionNotifier interface [Direct3D]","RegisterDestructionCallback method","ID3DDestructionNotifier.RegisterDestructionCallback","ID3DDestructionNotifier::RegisterDestructionCallback","RegisterDestructionCallback","RegisterDestructionCallback method [Direct3D]","RegisterDestructionCallback method [Direct3D]","ID3DDestructionNotifier interface","d3dcommon/ID3DDestructionNotifier::RegisterDestructionCallback","direct3d11.id3ddestructionnotifier_registerdestructioncallback"]
old-location: direct3d11\id3ddestructionnotifier_registerdestructioncallback.htm
tech.root: direct3d11
ms.assetid: 4d10c986-1cba-427c-ae90-f81b83be1b8b
ms.date: 12/05/2018
ms.keywords: ID3DDestructionNotifier interface [Direct3D],RegisterDestructionCallback method, ID3DDestructionNotifier.RegisterDestructionCallback, ID3DDestructionNotifier::RegisterDestructionCallback, RegisterDestructionCallback, RegisterDestructionCallback method [Direct3D], RegisterDestructionCallback method [Direct3D],ID3DDestructionNotifier interface, d3dcommon/ID3DDestructionNotifier::RegisterDestructionCallback, direct3d11.id3ddestructionnotifier_registerdestructioncallback
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
ms.custom: 19H1
f1_keywords:
 - ID3DDestructionNotifier::RegisterDestructionCallback
 - d3dcommon/ID3DDestructionNotifier::RegisterDestructionCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCommon.h
api_name:
 - ID3DDestructionNotifier.RegisterDestructionCallback
---

# ID3DDestructionNotifier::RegisterDestructionCallback


## -description

Registers a user-defined callback to be invoked when the object this **ID3DDestructionNotifier** was created from is destroyed.

## -parameters

### -param callbackFn

Type: <b>PFN_DESTRUCTION_CALLBACK</b>

A user-defined callback to be invoked when the object is destroyed.

### -param pData

Type: <b>void*</b>

The data to pass to **callbackFn** when invoked

### -param pCallbackID

Type: <b><a href="windows/desktop/WinProg/windows-data-types">UINT*</a></b>

Pointer to a **UINT** used to identify the callback, and can be passed to <a href="windows/desktop/api/d3dcommon/nf-d3dcommon-id3ddestructionnotifier-unregisterdestructioncallback"></a> to unregister the callback.

## -returns

Type: <b><a href="windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this function suceeds, it will return **S_OK**

## -remarks

An example of this interface being used to log the destruction of an **ID3D12Resource**

```cpp
#include <d3dcommon.h> // for ID3DDestructionNotifier

ComPtr<ID3D12Resource> resource = ...;

ComPtr<ID3DDestructionNotifier> notifier;
if (SUCCEEDED(resource.As(&notifier)))
{
    UINT callbackId;
    ThrowIfFailed(notifier->RegisterDestructionCallback(LogResourceReleased, nullptr, &callbackId));
}

void LogResourceReleased(void* context)
{
    OutputDebugString("Resource released!\n");
}
```

## -see-also

<a href="windows/desktop/api/d3dcommon/nn-d3dcommon-id3ddestructionnotifier">ID3DDestructionNotifier</a>



<a href="windows/desktop/api/d3dcommon/nf-d3dcommon-id3ddestructionnotifier-unregisterdestructioncallback">ID3DDestructionNotifier::UnregisterDestructionCallback</a>

