---
UID: NF:msinkaut.IInkRectangle.GetRectangle
title: IInkRectangle::GetRectangle (msinkaut.h)
description: Gets the elements of the InkRectangle object in a single call.
helpviewer_keywords: ["78efcd28-7095-49f7-b660-9744b1ccf93e","GetRectangle","GetRectangle method [Tablet PC]","GetRectangle method [Tablet PC]","IInkRectangle interface","IInkRectangle interface [Tablet PC]","GetRectangle method","IInkRectangle.GetRectangle","IInkRectangle::GetRectangle","msinkaut/IInkRectangle::GetRectangle","tablet.inkrectangle_getrectangle"]
old-location: tablet\inkrectangle_getrectangle.htm
tech.root: tablet
ms.assetid: 78efcd28-7095-49f7-b660-9744b1ccf93e
ms.date: 12/05/2018
ms.keywords: 78efcd28-7095-49f7-b660-9744b1ccf93e, GetRectangle, GetRectangle method [Tablet PC], GetRectangle method [Tablet PC],IInkRectangle interface, IInkRectangle interface [Tablet PC],GetRectangle method, IInkRectangle.GetRectangle, IInkRectangle::GetRectangle, msinkaut/IInkRectangle::GetRectangle, tablet.inkrectangle_getrectangle
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkRectangle::GetRectangle
 - msinkaut/IInkRectangle::GetRectangle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRectangle.GetRectangle
---

# IInkRectangle::GetRectangle


## -description

Gets the elements of the <a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object in a single call.

## -parameters

### -param Top [out]

The top of the rectangle.

### -param Left [out]

The left edge of the rectangle.

### -param Bottom [out]

The bottom of the rectangle.

### -param Right [out]

The right edge of the rectangle.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom">Bottom Property</a>



<a href="../msinkaut/nn-msinkaut-iinkrectangle.md">IInkRectangle</a>



<a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left">Left Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right">Right Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top">Top Property</a>
