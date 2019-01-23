---
UID: NF:dwrite_3.IDWriteFont3.GetFontFaceReference
title: IDWriteFont3::GetFontFaceReference
author: windows-sdk-content
description: Gets a font face reference that identifies this font.
old-location: directwrite\idwritefont3_getfontfacereference.htm
tech.root: DirectWrite
ms.assetid: 8939ADA0-B2D9-4489-B9AC-EA37776F6340
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFontFaceReference, GetFontFaceReference method [Direct Write], GetFontFaceReference method [Direct Write],IDWriteFont3 interface, IDWriteFont3 interface [Direct Write],GetFontFaceReference method, IDWriteFont3.GetFontFaceReference, IDWriteFont3::GetFontFaceReference, directwrite.idwritefont3_getfontfacereference, dwrite_3/IDWriteFont3::GetFontFaceReference
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
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
 - IDWriteFont3.GetFontFaceReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFont3::GetFontFaceReference


## -description


Gets a font face reference that identifies this font.


## -parameters




### -param fontFaceReference [out]

Type: <b><a href="https://msdn.microsoft.com/04242508-7439-43B6-B3E7-07617B782038">IDWriteFontFaceReference</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="https://msdn.microsoft.com/04242508-7439-43B6-B3E7-07617B782038">IDWriteFontFaceReference</a> interface for the newly created font face reference object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0BD21E3C-5F02-4A51-B64C-847B0DD5656B">IDWriteFont3</a>
 

 

