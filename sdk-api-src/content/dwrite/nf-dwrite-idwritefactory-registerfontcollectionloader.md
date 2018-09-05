---
UID: NF:dwrite.IDWriteFactory.RegisterFontCollectionLoader
title: IDWriteFactory::RegisterFontCollectionLoader
author: windows-sdk-content
description: Registers a custom font collection loader with the factory object.
old-location: directwrite\IDWriteFactory_RegisterFontCollectionLoader.htm
old-project: DirectWrite
ms.assetid: 495f8f56-42b6-4731-a26e-5da2c56a28ed
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDWriteFactory interface [Direct Write],RegisterFontCollectionLoader method, IDWriteFactory.RegisterFontCollectionLoader, IDWriteFactory::RegisterFontCollectionLoader, RegisterFontCollectionLoader, RegisterFontCollectionLoader method [Direct Write], RegisterFontCollectionLoader method [Direct Write],IDWriteFactory interface, directwrite.IDWriteFactory_RegisterFontCollectionLoader, dwrite/IDWriteFactory::RegisterFontCollectionLoader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFactory.RegisterFontCollectionLoader
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFactory::RegisterFontCollectionLoader


## -description


Registers a custom font collection loader with the factory object.


## -parameters




### -param fontCollectionLoader

Type: <b><a href="https://msdn.microsoft.com/898645ce-4bd5-4491-a31c-f60a17578872">IDWriteFontCollectionLoader</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/898645ce-4bd5-4491-a31c-f60a17578872">IDWriteFontCollectionLoader</a> object to be registered.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function registers a font collection loader with DirectWrite. The font collection loader interface, which should be implemented by a singleton object, 
      handles enumerating font files in a font collection given a particular type of key. A given instance can only be registered once. Succeeding attempts will return an error, 
      indicating that it has already been registered. Note that font file loader implementations must not register themselves with DirectWrite inside their constructors, 
      and must not unregister themselves inside their destructors, because registration and unregistraton operations increment and decrement the object reference count respectively. 
      Instead, registration and unregistration with DirectWrite of font file loaders should be performed outside of the font file loader implementation.



