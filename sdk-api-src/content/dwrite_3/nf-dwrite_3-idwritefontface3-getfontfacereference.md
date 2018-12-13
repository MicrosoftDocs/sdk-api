---
UID: NF:dwrite_3.IDWriteFontFace3.GetFontFaceReference
title: IDWriteFontFace3::GetFontFaceReference
author: windows-sdk-content
description: Gets a font face reference that identifies this font.
old-location: directwrite\idwritefontface3_getfontfacereference.htm
tech.root: DirectWrite
ms.assetid: 3830951F-B304-4EBC-B8D5-611D1AC87F63
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFontFaceReference, GetFontFaceReference method [Direct Write], GetFontFaceReference method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],GetFontFaceReference method, IDWriteFontFace3.GetFontFaceReference, IDWriteFontFace3::GetFontFaceReference, directwrite.idwritefontface3_getfontfacereference, dwrite_3/IDWriteFontFace3::GetFontFaceReference
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDWriteFontFace3.GetFontFaceReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFace3::GetFontFaceReference


## -description


Gets a font face reference that identifies this font.


## -parameters




### -param fontFaceReference [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn894576(v=VS.85).aspx">IDWriteFontFaceReference</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dn894576(v=VS.85).aspx">IDWriteFontFaceReference</a> interface for the newly created font face reference object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn894561(v=VS.85).aspx">IDWriteFontFace3</a>
 

 

