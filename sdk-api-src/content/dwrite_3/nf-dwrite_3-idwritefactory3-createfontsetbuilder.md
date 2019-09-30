---
UID: NF:dwrite_3.IDWriteFactory3.CreateFontSetBuilder
title: IDWriteFactory3::CreateFontSetBuilder (dwrite_3.h)
author: windows-sdk-content
description: Creates an empty font set builder to add font face references and create a custom font set.
old-location: directwrite\idwritefactory3_createfontsetbuilder.htm
tech.root: DirectWrite
ms.assetid: 8021f934-af83-ccd0-e142-455df88bf936
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateFontSetBuilder, CreateFontSetBuilder method [Direct Write], CreateFontSetBuilder method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],CreateFontSetBuilder method, IDWriteFactory3.CreateFontSetBuilder, IDWriteFactory3::CreateFontSetBuilder, directwrite.idwritefactory3_createfontsetbuilder, dwrite_3/IDWriteFactory3::CreateFontSetBuilder
ms.topic: method
f1_keywords: 
 - "dwrite_3/IDWriteFactory3.CreateFontSetBuilder"
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
 - IDWriteFactory3.CreateFontSetBuilder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFactory3::CreateFontSetBuilder


## -description


Creates an empty font set builder to add font face references     
  and create a custom font set. 


## -parameters




### -param fontSetBuilder [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder</a>**</b>

Holds the newly created font set builder object, or NULL in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a>
 

 

