---
UID: NF:dwrite_3.IDWriteFontFaceReference.CreateFontFace
title: IDWriteFontFaceReference::CreateFontFace
author: windows-sdk-content
description: Creates a font face from the reference for use with layout, shaping, or rendering.
old-location: directwrite\idwritefontfacereference_createfontface.htm
tech.root: DirectWrite
ms.assetid: f9bc5933-c766-5b30-e2cf-b276a80aecda
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateFontFace, CreateFontFace method [Direct Write], CreateFontFace method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],CreateFontFace method, IDWriteFontFaceReference.CreateFontFace, IDWriteFontFaceReference::CreateFontFace, directwrite.idwritefontfacereference_createfontface, dwrite_3/IDWriteFontFaceReference::CreateFontFace
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
 - IDWriteFontFaceReference.CreateFontFace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFaceReference::CreateFontFace


## -description


Creates a font face from the reference for use with layout, shaping, or rendering.


## -parameters




### -param fontFace [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn894561(v=VS.85).aspx">IDWriteFontFace3</a>**</b>

Newly created font face object, or nullptr in the case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function can fail with DWRITE_E_REMOTEFONT if the font is not local.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn894576(v=VS.85).aspx">IDWriteFontFaceReference</a>
 

 

