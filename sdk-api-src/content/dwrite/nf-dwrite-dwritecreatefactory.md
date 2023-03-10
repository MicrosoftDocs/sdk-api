---
UID: NF:dwrite.DWriteCreateFactory
title: DWriteCreateFactory function (dwrite.h)
description: Creates a DirectWrite factory object that is used for subsequent creation of individual DirectWrite objects.
helpviewer_keywords: ["DWriteCreateFactory","DWriteCreateFactory function [Direct Write]","directwrite.dwritecreatefactory","dwrite/DWriteCreateFactory"]
old-location: directwrite\dwritecreatefactory.htm
tech.root: DirectWrite
ms.assetid: c74c0906-0a5c-4ab8-87cf-a195566e1d9e
ms.date: 12/05/2018
ms.keywords: DWriteCreateFactory, DWriteCreateFactory function [Direct Write], directwrite.dwritecreatefactory, dwrite/DWriteCreateFactory
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWriteCreateFactory
 - dwrite/DWriteCreateFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dwrite.dll
api_name:
 - DWriteCreateFactory
---

# DWriteCreateFactory function


## -description

Creates a DirectWrite factory object that is used for subsequent creation of individual DirectWrite objects.

## -parameters

### -param factoryType [in]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b>

A value that specifies whether the factory object will be shared or isolated.

### -param iid [in]

Type: <b>REFIID</b>

A GUID value that identifies the DirectWrite factory interface, such as __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).

### -param factory [out]

Type: <b>IUnknown**</b>

An address of a pointer to the newly created DirectWrite factory object.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function creates a <a href="/windows/win32/DirectWrite/direct-write-portal">DirectWrite</a> factory object that is used for subsequent creation of individual DirectWrite objects.
 DirectWrite factory contains internal state data such as font loader registration and cached font data.
 In most cases it is recommended you use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state data, and thereby reduce memory usage.
 However, there are cases when it is desirable to reduce the impact of a component,
 such as a plug-in from an untrusted source, on the rest of the process, by sandboxing and isolating it from the rest of the process components. In such cases, it is recommended you use an isolated factory for the sandboxed component.

The following example shows how to create a shared <a href="/windows/win32/DirectWrite/direct-write-portal">DirectWrite</a> factory.


```cpp

if (SUCCEEDED(hr))
{
    hr = DWriteCreateFactory(
        DWRITE_FACTORY_TYPE_SHARED,
        __uuidof(IDWriteFactory),
        reinterpret_cast<IUnknown**>(&pDWriteFactory_)
        );
}


```

