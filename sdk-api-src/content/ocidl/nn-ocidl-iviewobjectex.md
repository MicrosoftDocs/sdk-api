---
UID: NN:ocidl.IViewObjectEx
title: IViewObjectEx (ocidl.h)
description: An extension derived from IViewObject2 to provide support for Enhanced, flicker-free drawing for non-rectangular objects and transparent objects, hit testing for non-rectangular objects, and Control sizinghelpviewer_keywords: ["IViewObjectEx","IViewObjectEx interface [COM]","IViewObjectEx interface [COM]","described","_ole_iviewobjectex","com.iviewobjectex","ocidl/IViewObjectEx"]
old-location: com\iviewobjectex.htm
tech.root: com
ms.assetid: 4e677ec6-9c9e-4ee7-bb7f-1df6e590319b
ms.date: 12/05/2018
ms.keywords: IViewObjectEx, IViewObjectEx interface [COM], IViewObjectEx interface [COM],described, _ole_iviewobjectex, com.iviewobjectex, ocidl/IViewObjectEx
f1_keywords:
- ocidl/IViewObjectEx
dev_langs:
- c++
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- OCIdl.h
api_name:
- IViewObjectEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IViewObjectEx interface


## -description


An extension derived from <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iviewobject2">IViewObject2</a> to provide support for:
<ul>
<li>Enhanced, flicker-free drawing for non-rectangular objects and transparent objects</li>
<li>Hit testing for non-rectangular objects</li>
<li>Control sizing</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IViewObjectEx</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iviewobject2">IViewObject2</a>. <b>IViewObjectEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IViewObjectEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-getnaturalextent">GetNaturalExtent</a>
</td>
<td align="left" width="63%">
Provides sizing hints from the container for the object to use as the user resizes it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-getrect">GetRect</a>
</td>
<td align="left" width="63%">
Retrieves a rectangle describing a requested drawing aspect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-getviewstatus">GetViewStatus</a>
</td>
<td align="left" width="63%">
Retrieves information about the opacity of the object, and what drawing aspects are supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-queryhitpoint">QueryHitPoint</a>
</td>
<td align="left" width="63%">
Indicates whether a point is within a given aspect of an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-queryhitrect">QueryHitRect</a>
</td>
<td align="left" width="63%">
Indicates whether any point in a rectangle is within a given drawing aspect of an object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iviewobject2">IViewObject2</a>
 

 

