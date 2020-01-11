---
UID: NN:dcomp.IDCompositionDevice3
title: IDCompositionDevice3 (dcomp.h)
description: Serves as a factory for all other Microsoft DirectComposition objects and provides methods to control transactional composition.
old-location: directcomp\idcompositiondevice3.htm
tech.root: directcomp
ms.assetid: 5da076dc-360d-0b28-f131-8669d1a91dd6
ms.date: 12/05/2018
ms.keywords: IDCompositionDevice3, IDCompositionDevice3 interface [DirectComposition], IDCompositionDevice3 interface [DirectComposition],described, dcomp/IDCompositionDevice3, directcomp.idcompositiondevice3
f1_keywords:
- dcomp/IDCompositionDevice3
dev_langs:
- c++
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dcomp.dll
api_name:
- IDCompositionDevice3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDevice3 interface


## -description


Serves as a factory for all other Microsoft DirectComposition objects and provides methods to control transactional composition.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionDevice3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>. <b>IDCompositionDevice3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionDevice3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-createaffinetransform2deffect">CreateAffineTransform2DEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionaffinetransform2deffect">IDCompositionAffineTransform2DEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-createarithmeticcompositeeffect">CreateArithmeticCompositeEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionarithmeticcompositeeffect">IDCompositionArithmeticCompositeEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-createblendeffect">CreateBlendEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionblendeffect">IDCompositionBlendEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-createbrightnesseffect">CreateBrightnessEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionbrightnesseffect">IDCompositionBrightnessEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-createcolormatrixeffect">CreateColorMatrixEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositioncolormatrixeffect">IDCompositionColorMatrixEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-createcompositeeffect">CreateCompositeEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositioncompositeeffect">IDCompositionCompositeEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn950133(v=vs.85)">CreateFloodEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn919732(v=vs.85)">IDCompositionFloodEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-creategaussianblureffect">CreateGaussianBlurEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiongaussianblureffect">IDCompositionGaussianBlurEffect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-createhuerotationeffect">CreateHueRotationEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionhuerotationeffect">IDCompositionHueRotationEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-createlineartransfereffect">CreateLinearTransferEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionlineartransfereffect">IDCompositionLinearTransferEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-createsaturationeffect">CreateSaturationEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionsaturationeffect">IDCompositionSaturationEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-createshadoweffect">CreateShadowEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionshadoweffect">IDCompositionShadowEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-createtabletransfereffect">CreateTableTransferEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontabletransfereffect">IDCompositionTableTransferEffect</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice3-createturbulenceeffect">CreateTurbulenceEffect</a>
</td>
<td align="left" width="63%">
Creates an instance of <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionturbulenceeffect">IDCompositionTurbulenceEffect</a>.
        

</td>
</tr>
</table> 

