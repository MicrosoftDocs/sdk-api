---
UID: NF:dwrite.IDWriteFactory.GetSystemFontCollection
title: IDWriteFactory::GetSystemFontCollection (dwrite.h)
description: Gets an object which represents the set of installed fonts.helpviewer_keywords: ["GetSystemFontCollection","GetSystemFontCollection method [Direct Write]","GetSystemFontCollection method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","GetSystemFontCollection method","IDWriteFactory.GetSystemFontCollection","IDWriteFactory::GetSystemFontCollection","directwrite.IDWriteFactory_GetSystemFontCollection","dwrite/IDWriteFactory::GetSystemFontCollection"]
old-location: directwrite\IDWriteFactory_GetSystemFontCollection.htm
tech.root: DirectWrite
ms.assetid: 4f5cbea1-9775-4266-aa3c-7c15892d61b1
ms.date: 12/05/2018
ms.keywords: GetSystemFontCollection, GetSystemFontCollection method [Direct Write], GetSystemFontCollection method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],GetSystemFontCollection method, IDWriteFactory.GetSystemFontCollection, IDWriteFactory::GetSystemFontCollection, directwrite.IDWriteFactory_GetSystemFontCollection, dwrite/IDWriteFactory::GetSystemFontCollection
f1_keywords:
- dwrite/IDWriteFactory.GetSystemFontCollection
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteFactory.GetSystemFontCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFactory::GetSystemFontCollection


## -description


 Gets an object which represents the set of installed fonts.


## -parameters




### -param fontCollection [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a>**</b>

When this method returns, contains the address of a pointer to the system font collection object, or <b>NULL</b> in case of failure.


### -param checkForUpdates

Type: <b>BOOL</b>

If this parameter is nonzero, the function performs an immediate check for changes to the set of
    installed fonts. If this parameter is <b>FALSE</b>, the function will still detect changes if the font cache service is running, but
     there may be some latency. For example, an application might specify <b>TRUE</b> if it has itself just installed a font and wants to 
     be sure the font collection contains that font.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>
 

 

