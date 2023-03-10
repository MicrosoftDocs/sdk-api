---
UID: NF:msinkaut.IInkRectangle.SetRectangle
title: IInkRectangle::SetRectangle (msinkaut.h)
description: Sets the elements of the InkRectangle object in a single call.
helpviewer_keywords: ["689ef8ea-3fa6-4fea-a4d8-2c59d23db9cf","IInkRectangle interface [Tablet PC]","SetRectangle method","IInkRectangle.SetRectangle","IInkRectangle::SetRectangle","SetRectangle","SetRectangle method [Tablet PC]","SetRectangle method [Tablet PC]","IInkRectangle interface","msinkaut/IInkRectangle::SetRectangle","tablet.inkrectangle_setrectangle"]
old-location: tablet\inkrectangle_setrectangle.htm
tech.root: tablet
ms.assetid: 689ef8ea-3fa6-4fea-a4d8-2c59d23db9cf
ms.date: 12/05/2018
ms.keywords: 689ef8ea-3fa6-4fea-a4d8-2c59d23db9cf, IInkRectangle interface [Tablet PC],SetRectangle method, IInkRectangle.SetRectangle, IInkRectangle::SetRectangle, SetRectangle, SetRectangle method [Tablet PC], SetRectangle method [Tablet PC],IInkRectangle interface, msinkaut/IInkRectangle::SetRectangle, tablet.inkrectangle_setrectangle
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
 - IInkRectangle::SetRectangle
 - msinkaut/IInkRectangle::SetRectangle
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
 - IInkRectangle.SetRectangle
---

# IInkRectangle::SetRectangle


## -description

Sets the elements of the <a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle</a> object in a single call.

## -parameters

### -param Top [in]

The top of the rectangle.

### -param Left [in]

The left of the rectangle.

### -param Bottom [in]

The bottom of the rectangle.

### -param Right [in]

The right of the rectangle.

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

## -remarks

<div class="alert"><b>Note</b>  The order of the parameters in this method (<i>Top</i>, <i>Left</i>, <i>Bottom</i>, and <i>Right</i>) is different from the expected order (<i>Left</i>, <i>Top</i>, <i>Right</i>, and <i>Bottom</i>).</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom">Bottom Property</a>



<a href="../msinkaut/nn-msinkaut-iinkrectangle.md">IInkRectangle</a>



<a href="/windows/desktop/tablet/inkrectangle-class">InkRectangle Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left">Left Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right">Right Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top">Top Property</a>
