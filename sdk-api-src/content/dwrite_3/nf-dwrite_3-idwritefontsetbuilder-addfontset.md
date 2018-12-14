---
UID: NF:dwrite_3.IDWriteFontSetBuilder.AddFontSet
title: IDWriteFontSetBuilder::AddFontSet
author: windows-sdk-content
description: Appends an existing font set to the one being built, allowing one to aggregate two sets or to essentially extend an existing one.
old-location: directwrite\idwritefontsetbuilder_addfontset.htm
tech.root: DirectWrite
ms.assetid: F8B94A1B-905B-4A96-9943-12BB516311C2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddFontSet, AddFontSet method [Direct Write], AddFontSet method [Direct Write],IDWriteFontSetBuilder interface, IDWriteFontSetBuilder interface [Direct Write],AddFontSet method, IDWriteFontSetBuilder.AddFontSet, IDWriteFontSetBuilder::AddFontSet, directwrite.idwritefontsetbuilder_addfontset, dwrite_3/IDWriteFontSetBuilder::AddFontSet
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDWriteFontSetBuilder.AddFontSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontSetBuilder::AddFontSet


## -description


Appends an existing font set to the one being built, allowing
        one to aggregate two sets or to essentially extend an existing one.


## -parameters




### -param fontSet [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn933235(v=VS.85).aspx">IDWriteFontSet</a>*</b>

Font set to append font face references from.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn933236(v=VS.85).aspx">IDWriteFontSetBuilder</a>
 

 

