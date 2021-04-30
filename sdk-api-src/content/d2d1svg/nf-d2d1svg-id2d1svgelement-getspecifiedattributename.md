---
UID: NF:d2d1svg.ID2D1SvgElement.GetSpecifiedAttributeName
title: ID2D1SvgElement::GetSpecifiedAttributeName (d2d1svg.h)
description: Gets the name of the attribute at the given index.
helpviewer_keywords: ["GetSpecifiedAttributeName","GetSpecifiedAttributeName method [Direct2D]","GetSpecifiedAttributeName method [Direct2D]","ID2D1SvgElement interface","ID2D1SvgElement interface [Direct2D]","GetSpecifiedAttributeName method","ID2D1SvgElement.GetSpecifiedAttributeName","ID2D1SvgElement::GetSpecifiedAttributeName","d2d1svg/ID2D1SvgElement::GetSpecifiedAttributeName","direct2d.id2d1svgelement_getspecifiedattributename"]
old-location: direct2d\id2d1svgelement_getspecifiedattributename.htm
tech.root: Direct2D
ms.assetid: 08419C4C-4EED-406F-884C-84532C6AF1CC
ms.date: 12/05/2018
ms.keywords: GetSpecifiedAttributeName, GetSpecifiedAttributeName method [Direct2D], GetSpecifiedAttributeName method [Direct2D],ID2D1SvgElement interface, ID2D1SvgElement interface [Direct2D],GetSpecifiedAttributeName method, ID2D1SvgElement.GetSpecifiedAttributeName, ID2D1SvgElement::GetSpecifiedAttributeName, d2d1svg/ID2D1SvgElement::GetSpecifiedAttributeName, direct2d.id2d1svgelement_getspecifiedattributename
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
 - ID2D1SvgElement::GetSpecifiedAttributeName
 - d2d1svg/ID2D1SvgElement::GetSpecifiedAttributeName
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
 - ID2D1SvgElement.GetSpecifiedAttributeName
---

# ID2D1SvgElement::GetSpecifiedAttributeName


## -description

Gets the name of the attribute at the given index.

## -parameters

### -param index

Type: <b>UINT32</b>

The index of the attribute.

### -param name [out]

Type: <b>PWSTR</b>

Outputs the name of the attribute.

### -param nameCount

Type: <b>UINT32</b>

Length of the string returned in the name argument.

### -param inherited [out, optional]

Type: <b>BOOL*</b>

Outputs whether the attribute is set to the inherit value.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/d2d1svg/nn-d2d1svg-id2d1svgelement">ID2D1SvgElement</a>