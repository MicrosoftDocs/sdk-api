---
UID: NF:dwrite_1.IDWriteFactory1.GetEudcFontCollection
title: IDWriteFactory1::GetEudcFontCollection
author: windows-sdk-content
description: Gets a font collection representing the set of EUDC (end-user defined characters) fonts.
old-location: directwrite\idwritefactory1_geteudcfontcollection.htm
tech.root: DirectWrite
ms.assetid: 7A0B476D-6158-4AE1-B66F-8168E4AE7DE4
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetEudcFontCollection, GetEudcFontCollection method [Direct Write], GetEudcFontCollection method [Direct Write],IDWriteFactory1 interface, IDWriteFactory1 interface [Direct Write],GetEudcFontCollection method, IDWriteFactory1.GetEudcFontCollection, IDWriteFactory1::GetEudcFontCollection, directwrite.idwritefactory1_geteudcfontcollection, dwrite_1/IDWriteFactory1::GetEudcFontCollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDWriteFactory1.GetEudcFontCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory1::GetEudcFontCollection


## -description


Gets a font collection representing the set of EUDC (end-user defined characters) fonts.


## -parameters




### -param fontCollection [out]

Type: <b><a href="https://msdn.microsoft.com/2ca7e2d3-d66a-4c57-8fbe-15a5232c3506">IDWriteFontCollection</a>**</b>

The font collection to fill.


### -param checkForUpdates

Type: <b>BOOL</b>

Whether to check for updates.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Note that if no EUDC is set on the system,
    the returned collection will be empty, meaning it will return success
    but GetFontFamilyCount will be zero.




## -see-also




<a href="https://msdn.microsoft.com/43FA7E32-FFAD-4F26-A225-811C2CC507DF">IDWriteFactory1</a>
 

 

