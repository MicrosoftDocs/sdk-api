---
UID: NF:d3dcommon.ID3DDestructionNotifier.RegisterDestructionCallback
title: ID3DDestructionNotifier::RegisterDestructionCallback (d3dcommon.h)
description: Registers a user-defined callback to be invoked on destruction of the object from which this [ID3DDestructionNotifier](/windows/win32/api/d3dcommon/nn-d3dcommon-id3ddestructionotifier) was created.
helpviewer_keywords: ["ID3DDestructionNotifier interface [Direct3D]","RegisterDestructionCallback method","ID3DDestructionNotifier.RegisterDestructionCallback","ID3DDestructionNotifier::RegisterDestructionCallback","RegisterDestructionCallback","RegisterDestructionCallback method [Direct3D]","RegisterDestructionCallback method [Direct3D]","ID3DDestructionNotifier interface","d3dcommon/ID3DDestructionNotifier::RegisterDestructionCallback","direct3d11.id3ddestructionnotifier_registerdestructioncallback"]
tech.root: direct3d11
ms.date: 10/06/2020
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
 - d3dcommon.h
api_name:
 - ID3DDestructionNotifier.RegisterDestructionCallback
---

## -description

Registers a user-defined callback to be invoked on destruction of the object from which this [ID3DDestructionNotifier](/windows/win32/api/d3dcommon/nn-d3dcommon-id3ddestructionotifier) was created.

## -parameters

### -param callbackFn

Type: <b>PFN_DESTRUCTION_CALLBACK</b>

A user-defined callback to be invoked when the object is destroyed.

### -param pData

Type: **void\***

The data to pass to *callbackFn* when invoked

### -param pCallbackID

Type: **[UINT](/windows/win32/winprog/windows-data-types)\***

Pointer to a **UINT** used to identify the callback, and to pass to <a href="/windows/win32/api/d3dcommon/nf-d3dcommon-id3ddestructionotifier-unregisterdestructioncallback"></a> to unregister the callback.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If this function succeeds, it returns **S_OK**.

## -remarks

An example of this interface being used to log the destruction of an **ID3D12Resource**.

```cppcx
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

<a href="/windows/win32/api/d3dcommon/nn-d3dcommon-id3ddestructionotifier">ID3DDestructionNotifier</a>

<a href="/windows/win32/api/d3dcommon/nf-d3dcommon-id3ddestructionotifier-unregisterdestructioncallback">ID3DDestructionNotifier::UnregisterDestructionCallback</a>
