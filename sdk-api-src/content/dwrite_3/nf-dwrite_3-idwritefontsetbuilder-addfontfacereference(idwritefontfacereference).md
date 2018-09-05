---
UID: NF:dwrite_3.IDWriteFontSetBuilder.AddFontFaceReference(IDWriteFontFaceReference)
title: IDWriteFontSetBuilder::AddFontFaceReference(IDWriteFontFaceReference)
author: windows-sdk-content
description: Adds a reference to a font to the set being built. The necessary metadata will automatically be extracted from the font upon calling CreateFontSet.
old-location: directwrite\idwritefontsetbuilder_addfontfacereference_1.htm
old-project: DirectWrite
ms.assetid: 0E67F5EF-F8BB-47D9-995D-40879351DC17
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: AddFontFaceReference, AddFontFaceReference method [Direct Write], AddFontFaceReference method [Direct Write],IDWriteFontSetBuilder interface, IDWriteFontSetBuilder interface [Direct Write],AddFontFaceReference method, IDWriteFontSetBuilder.AddFontFaceReference, IDWriteFontSetBuilder.AddFontFaceReference(IDWriteFontFaceReference), IDWriteFontSetBuilder::AddFontFaceReference, IDWriteFontSetBuilder::AddFontFaceReference(IDWriteFontFaceReference), directwrite.idwritefontsetbuilder_addfontfacereference_1, dwrite_3/IDWriteFontSetBuilder::AddFontFaceReference
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
 - IDWriteFontSetBuilder.AddFontFaceReference
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFontSetBuilder::AddFontFaceReference(IDWriteFontFaceReference)


## -description


Adds a reference to a font to the set being built. The necessary metadata will automatically be extracted from the font upon calling CreateFontSet.


## -parameters




### -param fontFaceReference [in]

Type: <b><a href="https://msdn.microsoft.com/04242508-7439-43B6-B3E7-07617B782038">IDWriteFontFaceReference</a>*</b>

Font face reference object to add to the set.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/CC6C95CA-BA8B-47C4-A241-650EC8477192">IDWriteFontSetBuilder</a>
 

 

