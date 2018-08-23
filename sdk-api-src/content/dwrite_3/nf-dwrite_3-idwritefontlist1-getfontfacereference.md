---
UID: NF:dwrite_3.IDWriteFontList1.GetFontFaceReference
title: IDWriteFontList1::GetFontFaceReference
author: windows-sdk-content
description: Gets a font face reference given its zero-based index.
old-location: directwrite\idwritefontlist1_getfontfacereference.htm
old-project: DirectWrite
ms.assetid: E8EFDD13-2B6E-4C50-9A5D-AFBB4C0AF08B
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetFontFaceReference, GetFontFaceReference method [Direct Write], GetFontFaceReference method [Direct Write],IDWriteFontList1 interface, IDWriteFontList1 interface [Direct Write],GetFontFaceReference method, IDWriteFontList1.GetFontFaceReference, IDWriteFontList1::GetFontFaceReference, directwrite.idwritefontlist1_getfontfacereference, dwrite_3/IDWriteFontList1::GetFontFaceReference
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFontList1.GetFontFaceReference
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFontList1::GetFontFaceReference


## -description


Gets a font face reference given its zero-based index.


## -parameters




### -param listIndex [in]

Type: <b>UINT32</b>

Zero-based index of the font in the font list.


### -param fontFaceReference [out]

Type: <b><a href="https://msdn.microsoft.com/04242508-7439-43B6-B3E7-07617B782038">IDWriteFontFaceReference</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="https://msdn.microsoft.com/04242508-7439-43B6-B3E7-07617B782038">IDWriteFontFaceReference</a> interface for the newly created font face reference object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/68B6B1E3-9463-4A45-853A-CCC9501E4301">IDWriteFontList1</a>
 

 

