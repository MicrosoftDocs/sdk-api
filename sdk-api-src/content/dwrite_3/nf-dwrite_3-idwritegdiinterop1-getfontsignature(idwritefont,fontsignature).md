---
UID: NF:dwrite_3.IDWriteGdiInterop1.GetFontSignature(IDWriteFont,FONTSIGNATURE)
title: IDWriteGdiInterop1::GetFontSignature(IDWriteFont,FONTSIGNATURE)
author: windows-sdk-content
description: Reads the font signature from the given font.
old-location: directwrite\idwritegdiinterop1_getfontsignature.htm
old-project: DirectWrite
ms.assetid: 205EC8E6-233B-4ADB-B6B5-E052CF75277A
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetFontSignature, GetFontSignature method [Direct Write], GetFontSignature method [Direct Write],IDWriteGdiInterop1 interface, IDWriteGdiInterop1 interface [Direct Write],GetFontSignature method, IDWriteGdiInterop1.GetFontSignature, IDWriteGdiInterop1.GetFontSignature(IDWriteFont,FONTSIGNATURE), IDWriteGdiInterop1::GetFontSignature, IDWriteGdiInterop1::GetFontSignature(IDWriteFont,FONTSIGNATURE), directwrite.idwritegdiinterop1_getfontsignature, dwrite_3/IDWriteGdiInterop1::GetFontSignature
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.redist: 
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
 - IDWriteGdiInterop1.GetFontSignature
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteGdiInterop1::GetFontSignature(IDWriteFont,FONTSIGNATURE)


## -description


Reads the font signature from the given font.


## -parameters




### -param font [in]

Type: <b><a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>*</b>

Font to read font signature from.


### -param fontSignature [out]

Type: <b>FONTSIGNATURE*</b>

Font signature from the OS/2 table, ulUnicodeRange and ulCodePageRange.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A69922D8-EF9F-4F46-91D3-F7F649CF4705">IDWriteGdiInterop1</a>
 

 

