---
UID: NN:d2d1_1.ID2D1Factory1
title: ID2D1Factory1 (d2d1_1.h)
description: Creates Direct2D resources.helpviewer_keywords: ["ID2D1Factory1","ID2D1Factory1 interface [Direct2D]","ID2D1Factory1 interface [Direct2D]","described","d2d1_1/ID2D1Factory1","direct2d.id2d1factory1"]
old-location: direct2d\id2d1factory1.htm
tech.root: Direct2D
ms.assetid: 8221c3b4-e331-403c-9406-ee8d3e103825
ms.date: 12/05/2018
ms.keywords: ID2D1Factory1, ID2D1Factory1 interface [Direct2D], ID2D1Factory1 interface [Direct2D],described, d2d1_1/ID2D1Factory1, direct2d.id2d1factory1
f1_keywords:
- d2d1_1/ID2D1Factory1
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1Factory1
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Factory1 interface


## -description


Creates Direct2D resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Factory1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>. <b>ID2D1Factory1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Factory1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-createdevice">CreateDevice</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1factory1-createdrawingstateblock-overload">CreateDrawingStateBlock</a>
</td>
<td align="left" width="63%">Overloaded. Creates a new drawing state block, this can be used in subsequent
    SaveDrawingState and RestoreDrawingState operations on the render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-creategdimetafile">CreateGdiMetafile</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafile">ID2D1GdiMetafile</a> object that you can use to replay metafile content. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-createpathgeometry">CreatePathGeometry</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1">ID2D1PathGeometry1</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1factory1-createstrokestyle-overload">CreateStrokeStyle</a>
</td>
<td align="left" width="63%">Overloaded. Creates a <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1">ID2D1StrokeStyle1</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-geteffectproperties">GetEffectProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties of an effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-getregisteredeffects">GetRegisteredEffects</a>
</td>
<td align="left" width="63%">
Returns the class IDs of the currently registered effects and global effects on this factory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstream">RegisterEffectFromStream</a>
</td>
<td align="left" width="63%">
Registers an effect within the factory instance with the property XML specified as a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring">RegisterEffectFromString</a>
</td>
<td align="left" width="63%">
Registers an effect within the factory instance with the property XML specified as a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-unregistereffect">UnregisterEffect</a>
</td>
<td align="left" width="63%">
Unregisters an  effect within the factory instance that corresponds to the <i>classId</i> provided. 

</td>
</tr>
</table> 


## -remarks



The <b>ID2D1Factory1</b> interface is used to create devices, register and unregister effects, and enumerate effects properties. Effects are registered and unregistered globally. The registration APIs are placed on this interface for convenience.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/multi-threaded-direct2d-apps">Multithreaded Direct2D Apps</a>
 

 

