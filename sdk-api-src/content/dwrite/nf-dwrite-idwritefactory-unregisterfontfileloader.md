---
UID: NF:dwrite.IDWriteFactory.UnregisterFontFileLoader
title: IDWriteFactory::UnregisterFontFileLoader
author: windows-sdk-content
description: Unregisters a font file loader that was previously registered with the DirectWrite font system using RegisterFontFileLoader.
old-location: directwrite\IDWriteFactory_UnregisterFontFileLoader.htm
tech.root: DirectWrite
ms.assetid: f048671e-dfb6-449d-9bcd-e5df8408c01a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteFactory interface [Direct Write],UnregisterFontFileLoader method, IDWriteFactory.UnregisterFontFileLoader, IDWriteFactory::UnregisterFontFileLoader, UnregisterFontFileLoader, UnregisterFontFileLoader method [Direct Write], UnregisterFontFileLoader method [Direct Write],IDWriteFactory interface, directwrite.IDWriteFactory_UnregisterFontFileLoader, dwrite/IDWriteFactory::UnregisterFontFileLoader
ms.topic: method
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
 - IDWriteFactory.UnregisterFontFileLoader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory::UnregisterFontFileLoader


## -description


 Unregisters a font file loader that was previously registered with the DirectWrite font system using <a href="https://msdn.microsoft.com/f5b28c3d-c3ad-4435-92c8-07841e8d160a">RegisterFontFileLoader</a>.


## -parameters




### -param fontFileLoader

Type: <b><a href="https://msdn.microsoft.com/855e281e-3855-4c11-af87-68f8e0dadbf8">IDWriteFontFileLoader</a>*</b>

Pointer to the file loader that was previously registered with the DirectWrite font system using <a href="https://msdn.microsoft.com/f5b28c3d-c3ad-4435-92c8-07841e8d160a">RegisterFontFileLoader</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 This function unregisters font file loader callbacks with the DirectWrite font system.
     You should implement the font file loader interface by a singleton object.
     Note that font file loader implementations must not register themselves with DirectWrite
     inside their constructors and must not unregister themselves in their destructors, because
     registration and unregistraton operations increment and decrement the object reference count respectively.
     Instead, registration and unregistration of font file loaders with DirectWrite should be performed
     outside of the font file loader implementation.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

