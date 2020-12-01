---
UID: NN:dcomp.IDCompositionEffectGroup
title: IDCompositionEffectGroup (dcomp.h)
description: Represents a group of bitmap effects that are applied together to modify the rasterization of a visual's subtree.
helpviewer_keywords: ["IDCompositionEffectGroup","IDCompositionEffectGroup interface [DirectComposition]","IDCompositionEffectGroup interface [DirectComposition]","described","dcomp/IDCompositionEffectGroup","directcomp.idcompositioneffectgroup"]
old-location: directcomp\idcompositioneffectgroup.htm
tech.root: directcomp
ms.assetid: B8C5A4D8-F161-4383-B117-B89E85C65B19
ms.date: 12/05/2018
ms.keywords: IDCompositionEffectGroup, IDCompositionEffectGroup interface [DirectComposition], IDCompositionEffectGroup interface [DirectComposition],described, dcomp/IDCompositionEffectGroup, directcomp.idcompositioneffectgroup
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionEffectGroup
 - dcomp/IDCompositionEffectGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionEffectGroup
---

# IDCompositionEffectGroup interface


## -description

Represents a group of bitmap effects that are applied together to modify the rasterization of a visual's subtree.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionEffectGroup</b> interface inherits from <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffect">IDCompositionEffect</a>. <b>IDCompositionEffectGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionEffectGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dcomp/nf-dcomp-setopacity">SetOpacity</a>
</td>
<td align="left" width="63%">Overloaded. Animates or changes the value of the Opacity property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d">SetTransform3D</a>
</td>
<td align="left" width="63%">
Sets the 3D transformation effect object that modifies the rasterization of the visuals that this effect group is applied to.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffect">IDCompositionEffect</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>