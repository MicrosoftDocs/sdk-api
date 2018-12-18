---
UID: NF:dwrite_3.IDWriteFontSetBuilder.CreateFontSet
title: IDWriteFontSetBuilder::CreateFontSet
author: windows-sdk-content
description: Creates a font set from all the font face references added so far with AddFontFaceReference.
old-location: directwrite\idwritefontsetbuilder_createfontset.htm
tech.root: DirectWrite
ms.assetid: 58923F9C-4DAA-4F97-AE25-A2560176E0F2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateFontSet, CreateFontSet method [Direct Write], CreateFontSet method [Direct Write],IDWriteFontSetBuilder interface, IDWriteFontSetBuilder interface [Direct Write],CreateFontSet method, IDWriteFontSetBuilder.CreateFontSet, IDWriteFontSetBuilder::CreateFontSet, directwrite.idwritefontsetbuilder_createfontset, dwrite_3/IDWriteFontSetBuilder::CreateFontSet
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
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
 - IDWriteFontSetBuilder.CreateFontSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontSetBuilder::CreateFontSet


## -description


Creates a font set from all the font face references added so
        far with AddFontFaceReference.


## -parameters




### -param fontSet [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn933235(v=VS.85).aspx">IDWriteFontSet</a>**</b>

Contains the newly created font set object, or nullptr in case of failure.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creating a font set takes less time if the references were added with metadata rather than needing to extract the metadata from the
      font file.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn933236(v=VS.85).aspx">IDWriteFontSetBuilder</a>
 

 

