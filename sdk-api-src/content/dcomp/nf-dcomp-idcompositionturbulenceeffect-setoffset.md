---
UID: NF:dcomp.IDCompositionTurbulenceEffect.SetOffset
title: IDCompositionTurbulenceEffect::SetOffset (dcomp.h)
author: windows-sdk-content
description: Sets the coordinates where the turbulence output is generated.
old-location: directcomp\idcompositionturbulenceeffect_setoffset.htm
tech.root: directcomp
ms.assetid: 6C27C707-93CE-4EAD-ACFB-2DA36EFB1FB5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionTurbulenceEffect interface [DirectComposition],SetOffset method, IDCompositionTurbulenceEffect.SetOffset, IDCompositionTurbulenceEffect::SetOffset, SetOffset, SetOffset method [DirectComposition], SetOffset method [DirectComposition],IDCompositionTurbulenceEffect interface, dcomp/IDCompositionTurbulenceEffect::SetOffset, directcomp.idcompositionturbulenceeffect_setoffset
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionTurbulenceEffect.SetOffset"
req.header: dcomp.h
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
 - IDCompositionTurbulenceEffect.SetOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionTurbulenceEffect::SetOffset


## -description


Sets the coordinates where the turbulence output is generated.


## -parameters




### -param offset [in, ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a></b>

The coordinates where the turbulence output is generated.
            The algorithm used to generate the Perlin noise is position dependent, so a different offset results in a different output. This value is not bounded and the units are specified in DIPs
            

<div class="alert"><b>Note</b>  Note  The offset does not have the same effect as a translation because the noise function output is infinite and the function will wrap around the tile.</div>
<div> </div>

## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionturbulenceeffect">IDCompositionTurbulenceEffect</a>
 

 

