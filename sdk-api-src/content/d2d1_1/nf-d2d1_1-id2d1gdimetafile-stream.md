---
UID: NF:d2d1_1.ID2D1GdiMetafile.Stream
title: ID2D1GdiMetafile::Stream (d2d1_1.h)
description: This method streams the contents of the command to the given metafile sink.
helpviewer_keywords: ["ID2D1GdiMetafile interface [Direct2D]","Stream method","ID2D1GdiMetafile.Stream","ID2D1GdiMetafile::Stream","Stream","Stream method [Direct2D]","Stream method [Direct2D]","ID2D1GdiMetafile interface","d2d1_1/ID2D1GdiMetafile::Stream","direct2d.id2d1gdimetafile_stream"]
old-location: direct2d\id2d1gdimetafile_stream.htm
tech.root: Direct2D
ms.assetid: 84E7305D-1E2D-43C3-8E79-02EBCC8F36A1
ms.date: 12/05/2018
ms.keywords: ID2D1GdiMetafile interface [Direct2D],Stream method, ID2D1GdiMetafile.Stream, ID2D1GdiMetafile::Stream, Stream, Stream method [Direct2D], Stream method [Direct2D],ID2D1GdiMetafile interface, d2d1_1/ID2D1GdiMetafile::Stream, direct2d.id2d1gdimetafile_stream
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1GdiMetafile::Stream
 - d2d1_1/ID2D1GdiMetafile::Stream
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
 - ID2D1GdiMetafile.Stream
---

# ID2D1GdiMetafile::Stream


## -description

This method streams the contents of the command  to the given metafile  sink.

## -parameters

### -param sink

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafilesink">ID2D1GdiMetafileSink</a></b>

The sink into which Direct2D  will call back.

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

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafile">ID2D1GdiMetafile</a>