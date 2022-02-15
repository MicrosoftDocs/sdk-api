---
UID: NN:dwrite.IDWriteFontCollectionLoader
title: IDWriteFontCollectionLoader (dwrite.h)
description: Used to construct a collection of fonts given a particular type of key.
helpviewer_keywords: ["IDWriteFontCollectionLoader","IDWriteFontCollectionLoader interface [Direct Write]","IDWriteFontCollectionLoader interface [Direct Write]","described","directwrite.IDWriteFontCollectionLoader","dwrite/IDWriteFontCollectionLoader"]
old-location: directwrite\IDWriteFontCollectionLoader.htm
tech.root: DirectWrite
ms.assetid: 898645ce-4bd5-4491-a31c-f60a17578872
ms.date: 12/05/2018
ms.keywords: IDWriteFontCollectionLoader, IDWriteFontCollectionLoader interface [Direct Write], IDWriteFontCollectionLoader interface [Direct Write],described, directwrite.IDWriteFontCollectionLoader, dwrite/IDWriteFontCollectionLoader
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
 - IDWriteFontCollectionLoader
 - dwrite/IDWriteFontCollectionLoader
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
 - IDWriteFontCollectionLoader
---

# IDWriteFontCollectionLoader interface


## -description

  Used to construct a collection of fonts given a particular type of key.

## -inheritance

The <b>IDWriteFontCollectionLoader</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFontCollectionLoader</b> also has these types of members:

## -remarks

The font collection loader interface is recommended to be implemented by a singleton object. Note that font collection loader implementations must not register themselves with DirectWrite factory inside their constructors and must not unregister themselves in their destructors, because registration and unregistration operations increment and decrement the object reference count respectively. Instead, registration and unregistration of font file loaders with DirectWrite factory should be performed outside of the font file loader implementation as a separate step.

