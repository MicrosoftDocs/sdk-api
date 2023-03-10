---
UID: NF:d2d1_1.ID2D1Factory1.CreatePathGeometry
title: ID2D1Factory1::CreatePathGeometry (d2d1_1.h)
description: Creates an ID2D1PathGeometry1 object.
helpviewer_keywords: ["CreatePathGeometry","CreatePathGeometry method [Direct2D]","CreatePathGeometry method [Direct2D]","ID2D1Factory1 interface","ID2D1Factory1 interface [Direct2D]","CreatePathGeometry method","ID2D1Factory1.CreatePathGeometry","ID2D1Factory1::CreatePathGeometry","d2d1_1/ID2D1Factory1::CreatePathGeometry","direct2d.id2d1factory1_createpathgeometry"]
old-location: direct2d\id2d1factory1_createpathgeometry.htm
tech.root: Direct2D
ms.assetid: 182e7dbc-ab49-427f-8801-d94e4ed9a308
ms.date: 12/05/2018
ms.keywords: CreatePathGeometry, CreatePathGeometry method [Direct2D], CreatePathGeometry method [Direct2D],ID2D1Factory1 interface, ID2D1Factory1 interface [Direct2D],CreatePathGeometry method, ID2D1Factory1.CreatePathGeometry, ID2D1Factory1::CreatePathGeometry, d2d1_1/ID2D1Factory1::CreatePathGeometry, direct2d.id2d1factory1_createpathgeometry
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory1::CreatePathGeometry
 - d2d1_1/ID2D1Factory1::CreatePathGeometry
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
 - ID2D1Factory1.CreatePathGeometry
---

# ID2D1Factory1::CreatePathGeometry


## -description

Creates an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1">ID2D1PathGeometry1</a> object.

## -parameters

### -param pathGeometry [out]

Type: <b>const **</b>

When this method returns, contains the address of a pointer to the newly created path geometry.

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
</table>

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1">ID2D1Factory1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1">ID2D1PathGeometry1</a>