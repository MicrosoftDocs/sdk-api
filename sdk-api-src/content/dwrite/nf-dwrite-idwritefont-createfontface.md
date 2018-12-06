---
UID: NF:dwrite.IDWriteFont.CreateFontFace
title: IDWriteFont::CreateFontFace
author: windows-sdk-content
description: Creates a font face object for the font.
old-location: directwrite\IDWriteFont_CreateFontFace.htm
tech.root: DirectWrite
ms.assetid: dd70a9f7-43f3-43e9-94d9-fe70b1b53f59
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateFontFace, CreateFontFace method [Direct Write], CreateFontFace method [Direct Write],IDWriteFont interface, IDWriteFont interface [Direct Write],CreateFontFace method, IDWriteFont.CreateFontFace, IDWriteFont::CreateFontFace, directwrite.IDWriteFont_CreateFontFace, dwrite/IDWriteFont::CreateFontFace
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDWriteFont.CreateFontFace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFont::CreateFontFace


## -description


 Creates a font face object for the font.


## -parameters




### -param fontFace [out]

Type: <b><a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>**</b>

When this method returns, contains an address of a pointer to the newly created font face object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>
 

 

