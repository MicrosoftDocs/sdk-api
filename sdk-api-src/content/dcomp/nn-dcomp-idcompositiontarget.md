---
UID: NN:dcomp.IDCompositionTarget
title: IDCompositionTarget (dcomp.h)
description: Represents a binding between a Microsoft DirectComposition visual tree and a destination on top of which the visual tree should be composed.
helpviewer_keywords: ["IDCompositionTarget","IDCompositionTarget interface [DirectComposition]","IDCompositionTarget interface [DirectComposition]","described","dcomp/IDCompositionTarget","directcomp.idcompositiontarget"]
old-location: directcomp\idcompositiontarget.htm
tech.root: directcomp
ms.assetid: 86dbfe68-e360-42cf-b572-960398ef06ba
ms.date: 12/05/2018
ms.keywords: IDCompositionTarget, IDCompositionTarget interface [DirectComposition], IDCompositionTarget interface [DirectComposition],described, dcomp/IDCompositionTarget, directcomp.idcompositiontarget
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
 - IDCompositionTarget
 - dcomp/IDCompositionTarget
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
 - IDCompositionTarget
---

# IDCompositionTarget interface


## -description

Represents a binding between a Microsoft DirectComposition visual tree and a destination on top of which the visual tree should be composed.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionTarget</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDCompositionTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiontarget-setroot">SetRoot</a>
</td>
<td align="left" width="63%">
Sets a visual object as the new root object of a visual tree.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd">IDCompositionDevice::CreateTargetForHwnd</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>