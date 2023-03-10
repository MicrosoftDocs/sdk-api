---
UID: NN:dwrite.IDWriteFontFileLoader
title: IDWriteFontFileLoader (dwrite.h)
description: Handles loading font file resources of a particular type from a font file reference key into a font file stream object.
helpviewer_keywords: ["IDWriteFontFileLoader","IDWriteFontFileLoader interface [Direct Write]","IDWriteFontFileLoader interface [Direct Write]","described","directwrite.IDWriteFontFileLoader","dwrite/IDWriteFontFileLoader"]
old-location: directwrite\IDWriteFontFileLoader.htm
tech.root: DirectWrite
ms.assetid: 855e281e-3855-4c11-af87-68f8e0dadbf8
ms.date: 12/05/2018
ms.keywords: IDWriteFontFileLoader, IDWriteFontFileLoader interface [Direct Write], IDWriteFontFileLoader interface [Direct Write],described, directwrite.IDWriteFontFileLoader, dwrite/IDWriteFontFileLoader
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
 - IDWriteFontFileLoader
 - dwrite/IDWriteFontFileLoader
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
 - IDWriteFontFileLoader
---

# IDWriteFontFileLoader interface


## -description

 Handles loading font file resources of a particular type from a font file reference key into a font file stream object.

## -inheritance

The <b>IDWriteFontFileLoader</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFontFileLoader</b> also has these types of members:

## -remarks

The font file loader interface is recommended to be implemented by a singleton object. Note that font file loader implementations must not register themselves with DirectWrite factory inside their constructors and must not unregister themselves in their destructors, because registration and unregistration operations increment and decrement the object reference count respectively. Instead, registration and unregistration of font file loaders with DirectWrite factory should be performed outside of the font file loader implementation as a separate step.

