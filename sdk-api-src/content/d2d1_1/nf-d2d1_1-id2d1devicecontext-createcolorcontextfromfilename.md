---
UID: NF:d2d1_1.ID2D1DeviceContext.CreateColorContextFromFilename
title: ID2D1DeviceContext::CreateColorContextFromFilename (d2d1_1.h)
description: Creates a color context by loading it from the specified filename. The profile bytes are the contents of the file specified by Filename.
helpviewer_keywords: ["CreateColorContextFromFilename","CreateColorContextFromFilename method [Direct2D]","CreateColorContextFromFilename method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","CreateColorContextFromFilename method","ID2D1DeviceContext.CreateColorContextFromFilename","ID2D1DeviceContext::CreateColorContextFromFilename","d2d1_1/ID2D1DeviceContext::CreateColorContextFromFilename","direct2d.id2d1devicecontext_createcolorcontextfromfilename"]
old-location: direct2d\id2d1devicecontext_createcolorcontextfromfilename.htm
tech.root: Direct2D
ms.assetid: ae72c68a-d984-4287-b607-a18913f083d4
ms.date: 12/05/2018
ms.keywords: CreateColorContextFromFilename, CreateColorContextFromFilename method [Direct2D], CreateColorContextFromFilename method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],CreateColorContextFromFilename method, ID2D1DeviceContext.CreateColorContextFromFilename, ID2D1DeviceContext::CreateColorContextFromFilename, d2d1_1/ID2D1DeviceContext::CreateColorContextFromFilename, direct2d.id2d1devicecontext_createcolorcontextfromfilename
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
 - ID2D1DeviceContext::CreateColorContextFromFilename
 - d2d1_1/ID2D1DeviceContext::CreateColorContextFromFilename
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
 - ID2D1DeviceContext.CreateColorContextFromFilename
---

# ID2D1DeviceContext::CreateColorContextFromFilename


## -description

Creates a color context by loading it from the specified filename.  The profile bytes are the contents of the file specified by <i>Filename</i>.

## -parameters

### -param filename

Type: <b>PCWSTR</b>

The path to the file containing the profile bytes to initialize the color context with.

### -param colorContext [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1colorcontext">ID2D1ColorContext</a>**</b>

When this method returns, contains the address of a pointer to a new color context.

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

## -remarks

The new color context can be used in <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1">D2D1_BITMAP_PROPERTIES1</a> to initialize the color context of a created bitmap.  The model field of the profile header is inspected to determine whether this profile is sRGB or scRGB and the color space is updated respectively.  Otherwise the space is  custom.

## -see-also

<a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1">D2D1_BITMAP_PROPERTIES1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1bitmap1">ID2D1Bitmap1</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>