---
UID: NF:dwrite_3.IDWriteFontSet.FindFontFaceReference
title: IDWriteFontSet::FindFontFaceReference
author: windows-sdk-content
description: Gets the index of the matching font face reference in the font set, with the same file, face index, and simulations.
old-location: directwrite\idwritefontset_findfontfacereference.htm
old-project: DirectWrite
ms.assetid: dba55a36-8037-5564-59d8-e01189ff0020
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: FindFontFaceReference, FindFontFaceReference method [Direct Write], FindFontFaceReference method [Direct Write],IDWriteFontSet interface, IDWriteFontSet interface [Direct Write],FindFontFaceReference method, IDWriteFontSet.FindFontFaceReference, IDWriteFontSet::FindFontFaceReference, directwrite.idwritefontset_findfontfacereference, dwrite_3/IDWriteFontSet::FindFontFaceReference
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
 - IDWriteFontSet.FindFontFaceReference
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFontSet::FindFontFaceReference


## -description


Gets the index of the matching font face reference in the font set, with the same file, face index, and simulations.


## -parameters




### -param fontFaceReference

Type: <b><a href="https://msdn.microsoft.com/04242508-7439-43B6-B3E7-07617B782038">IDWriteFontFaceReference</a>*</b>

Font face object that specifies the physical font.


### -param listIndex [out]

Type: <b>UINT32*</b>

Receives the zero-based index of the matching font if the font was found, or UINT_MAX otherwise.


### -param exists [out]

Type: <b>BOOL*</b>

Receives TRUE if the font exists or FALSE otherwise.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0178f248-8dc0-c0ee-63c1-8db3f6ef94c3">IDWriteFontSet</a>
 

 

