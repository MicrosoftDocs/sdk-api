---
UID: NF:dwrite.IDWriteFontFace.ReleaseFontTable
title: IDWriteFontFace::ReleaseFontTable (dwrite.h)
description: Releases the table obtained earlier from TryGetFontTable.
helpviewer_keywords: ["IDWriteFontFace interface [Direct Write]","ReleaseFontTable method","IDWriteFontFace.ReleaseFontTable","IDWriteFontFace::ReleaseFontTable","ReleaseFontTable","ReleaseFontTable method [Direct Write]","ReleaseFontTable method [Direct Write]","IDWriteFontFace interface","directwrite.IDWriteFontFace_ReleaseFontTable","dwrite/IDWriteFontFace::ReleaseFontTable"]
old-location: directwrite\IDWriteFontFace_ReleaseFontTable.htm
tech.root: DirectWrite
ms.assetid: 6e9b7e30-eae9-476b-89bd-a794e08ba468
ms.date: 12/05/2018
ms.keywords: IDWriteFontFace interface [Direct Write],ReleaseFontTable method, IDWriteFontFace.ReleaseFontTable, IDWriteFontFace::ReleaseFontTable, ReleaseFontTable, ReleaseFontTable method [Direct Write], ReleaseFontTable method [Direct Write],IDWriteFontFace interface, directwrite.IDWriteFontFace_ReleaseFontTable, dwrite/IDWriteFontFace::ReleaseFontTable
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontFace::ReleaseFontTable
 - dwrite/IDWriteFontFace::ReleaseFontTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFace.ReleaseFontTable
---

# IDWriteFontFace::ReleaseFontTable


## -description

 Releases the table obtained earlier from <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-trygetfonttable">TryGetFontTable</a>.

## -parameters

### -param tableContext [in]

Type: <b>void*</b>

A pointer to the opaque context from <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-trygetfonttable">TryGetFontTable</a>.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>

