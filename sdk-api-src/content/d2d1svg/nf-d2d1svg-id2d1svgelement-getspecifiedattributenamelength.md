---
UID: NF:d2d1svg.ID2D1SvgElement.GetSpecifiedAttributeNameLength
title: ID2D1SvgElement::GetSpecifiedAttributeNameLength (d2d1svg.h)
description: Gets the string length of the name of the specified attribute at the given index.
helpviewer_keywords: ["GetSpecifiedAttributeNameLength","GetSpecifiedAttributeNameLength method [Direct2D]","GetSpecifiedAttributeNameLength method [Direct2D]","ID2D1SvgElement interface","ID2D1SvgElement interface [Direct2D]","GetSpecifiedAttributeNameLength method","ID2D1SvgElement.GetSpecifiedAttributeNameLength","ID2D1SvgElement::GetSpecifiedAttributeNameLength","d2d1svg/ID2D1SvgElement::GetSpecifiedAttributeNameLength","direct2d.id2d1svgelement_getspecifiedattributenamelength"]
old-location: direct2d\id2d1svgelement_getspecifiedattributenamelength.htm
tech.root: Direct2D
ms.assetid: AD94B020-D9AA-4B1F-B7C3-DEF97DADFEEA
ms.date: 12/05/2018
ms.keywords: GetSpecifiedAttributeNameLength, GetSpecifiedAttributeNameLength method [Direct2D], GetSpecifiedAttributeNameLength method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetSpecifiedAttributeNameLength method, ID2D1SvgElement.GetSpecifiedAttributeNameLength, ID2D1SvgElement::GetSpecifiedAttributeNameLength, d2d1svg/ID2D1SvgElement::GetSpecifiedAttributeNameLength, direct2d.id2d1svgelement_getspecifiedattributenamelength
req.header: d2d1svg.h
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
req.lib: 
req.dll: Direct2d.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1SvgElement::GetSpecifiedAttributeNameLength
 - d2d1svg/ID2D1SvgElement::GetSpecifiedAttributeNameLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgElement.GetSpecifiedAttributeNameLength
---

# ID2D1SvgElement::GetSpecifiedAttributeNameLength


## -description

Gets the string length of the name of the specified attribute at the given index. The output string length does not include room for the null terminator.

## -parameters

### -param index

Type: <b>UINT32</b>

The index of the attribute.

### -param nameLength [out]

Type: <b>UINT32*</b>

Outputs the string length of the name of the specified attribute.

### -param inherited [out, optional]

Type: <b>BOOL*</b>

Indicates whether the attribute is set to the inherit value.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>