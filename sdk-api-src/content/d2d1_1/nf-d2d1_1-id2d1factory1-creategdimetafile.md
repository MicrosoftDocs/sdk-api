---
UID: NF:d2d1_1.ID2D1Factory1.CreateGdiMetafile
title: ID2D1Factory1::CreateGdiMetafile (d2d1_1.h)
description: Creates a new ID2D1GdiMetafile object that you can use to replay metafile content.
helpviewer_keywords: ["CreateGdiMetafile","CreateGdiMetafile method [Direct2D]","CreateGdiMetafile method [Direct2D]","ID2D1Factory1 interface","ID2D1Factory1 interface [Direct2D]","CreateGdiMetafile method","ID2D1Factory1.CreateGdiMetafile","ID2D1Factory1::CreateGdiMetafile","d2d1_1/ID2D1Factory1::CreateGdiMetafile","direct2d.id2d1factory1_creategdimetafile"]
old-location: direct2d\id2d1factory1_creategdimetafile.htm
tech.root: Direct2D
ms.assetid: 580DF262-2A86-4C21-8DFA-A804CE0A79CC
ms.date: 12/05/2018
ms.keywords: CreateGdiMetafile, CreateGdiMetafile method [Direct2D], CreateGdiMetafile method [Direct2D],ID2D1Factory1 interface, ID2D1Factory1 interface [Direct2D],CreateGdiMetafile method, ID2D1Factory1.CreateGdiMetafile, ID2D1Factory1::CreateGdiMetafile, d2d1_1/ID2D1Factory1::CreateGdiMetafile, direct2d.id2d1factory1_creategdimetafile
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory1::CreateGdiMetafile
 - d2d1_1/ID2D1Factory1::CreateGdiMetafile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory1.CreateGdiMetafile
---

# ID2D1Factory1::CreateGdiMetafile


## -description

Creates a new <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafile">ID2D1GdiMetafile</a> object that you can use to replay metafile content.

## -parameters

### -param metafileStream [in]

Type: <b>IStream*</b>

A stream object that has the metafile data.

### -param metafile [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafile">ID2D1GdiMetafile</a>**</b>

The address of the newly created GDI metafile object.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid value was passed to the method.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1">ID2D1Factory1</a>