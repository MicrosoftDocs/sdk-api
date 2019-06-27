---
UID: NF:dwrite_3.IDWriteFontSetBuilder.AddFontSet
title: IDWriteFontSetBuilder::AddFontSet (dwrite_3.h)
author: windows-sdk-content
description: Appends an existing font set to the one being built, allowing one to aggregate two sets or to essentially extend an existing one.
old-location: directwrite\idwritefontsetbuilder_addfontset.htm
tech.root: DirectWrite
ms.assetid: F8B94A1B-905B-4A96-9943-12BB516311C2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddFontSet, AddFontSet method [Direct Write], AddFontSet method [Direct Write],IDWriteFontSetBuilder interface, IDWriteFontSetBuilder interface [Direct Write],AddFontSet method, IDWriteFontSetBuilder.AddFontSet, IDWriteFontSetBuilder::AddFontSet, directwrite.idwritefontsetbuilder_addfontset, dwrite_3/IDWriteFontSetBuilder::AddFontSet
ms.topic: method
f1_keywords: 
 - "dwrite_3/IDWriteFontSetBuilder.AddFontSet"
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
 - IDWriteFontSetBuilder.AddFontSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontSetBuilder::AddFontSet


## -description


Appends an existing font set to the one being built, allowing
        one to aggregate two sets or to essentially extend an existing one.


## -parameters




### -param fontSet [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>*</b>

Font set to append font face references from.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder</a>
 

 

