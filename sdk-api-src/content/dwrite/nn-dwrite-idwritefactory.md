---
UID: NN:dwrite.IDWriteFactory
title: IDWriteFactory (dwrite.h)
description: Used to create all subsequent DirectWrite objects. This interface is the root factory interface for all DirectWrite objects.
helpviewer_keywords: ["IDWriteFactory","IDWriteFactory interface [Direct Write]","IDWriteFactory interface [Direct Write]","described","directwrite.IDWriteFactory","dwrite/IDWriteFactory"]
old-location: directwrite\IDWriteFactory.htm
tech.root: DirectWrite
ms.assetid: 73a85977-5c24-4abc-ad8c-1d0d6474bd7e
ms.date: 12/05/2018
ms.keywords: IDWriteFactory, IDWriteFactory interface [Direct Write], IDWriteFactory interface [Direct Write],described, directwrite.IDWriteFactory, dwrite/IDWriteFactory
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
 - IDWriteFactory
 - dwrite/IDWriteFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFactory
---

# IDWriteFactory interface


## -description

Used to create all subsequent DirectWrite objects. This interface is the root factory interface for all DirectWrite objects.

## -inheritance

The <b>IDWriteFactory</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFactory</b> also has these types of members:

## -remarks

Create an <b>IDWriteFactory</b> object by using the <a href="/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory">DWriteCreateFactory</a> function.  


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


An <b>IDWriteFactory</b> object holds state information, such as font loader registration and cached font data.  This state can be shared or isolated.  Shared is recommended for most applications because it saves memory.  However, isolated can be useful in situations where you want to have a separate state for some objects.

