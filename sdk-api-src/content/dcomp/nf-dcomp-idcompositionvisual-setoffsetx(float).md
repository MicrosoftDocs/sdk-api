---
UID: NF:dcomp.IDCompositionVisual.SetOffsetX(float)
title: IDCompositionVisual::SetOffsetX(float) (dcomp.h)
description: Changes the value of the OffsetX property of this visual. (overload 1/2)
helpviewer_keywords: ["IDCompositionVisual interface [DirectComposition]","SetOffsetX method","IDCompositionVisual.SetOffsetX","IDCompositionVisual.SetOffsetX(float)","IDCompositionVisual::SetOffsetX","IDCompositionVisual::SetOffsetX(float)","SetOffsetX","SetOffsetX method [DirectComposition]","SetOffsetX method [DirectComposition]","IDCompositionVisual interface","dcomp/IDCompositionVisual::SetOffsetX","directcomp.idcompositionvisual_setoffsetx_float"]
old-location: directcomp\idcompositionvisual_setoffsetx_float.htm
tech.root: directcomp
ms.assetid: 5A90D9F4-E28D-49D6-9E5A-511E9479BD97
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetOffsetX method, IDCompositionVisual.SetOffsetX, IDCompositionVisual.SetOffsetX(float), IDCompositionVisual::SetOffsetX, IDCompositionVisual::SetOffsetX(float), SetOffsetX, SetOffsetX method [DirectComposition], SetOffsetX method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetOffsetX, directcomp.idcompositionvisual_setoffsetx_float
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
 - IDCompositionVisual::SetOffsetX
 - dcomp/IDCompositionVisual::SetOffsetX
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
 - IDCompositionVisual.SetOffsetX
---

# IDCompositionVisual::SetOffsetX(float)


## -description

Changes the value of the OffsetX property of this visual.  The OffsetX property specifies the new offset of the visual along the x-axis, relative to the parent visual.

## -parameters

### -param offsetX [in]

Type: <b>float</b>

The new offset of the visual along the x-axis, in pixels.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>offsetX</i> parameter is NaN, positive infinity, or negative infinity.



Changing the OffsetX property of a visual transforms the coordinate system of the entire visual subtree that is rooted at that visual. If the Clip property of this visual is specified, the clip rectangle is also transformed.





A transformation that is specified by the Transform property is applied after the OffsetX property.  In other words, the effect of setting the Transform property and the OffsetX property is the same as setting only the Transform property on a transform group  object where the first member of the group is an <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform">IDCompositionTranslateTransform</a> object that has the same OffsetX value as <i>offsetX</i>. However, you should use  <b>IDCompositionVisual::SetOffsetX</b> whenever possible because it is slightly faster.

If the OffsetX and OffsetY properties are set to 0, and the Transform property is set to NULL, the coordinate system of the visual is the same as that of its parent.

If the OffsetX property was previously animated, this method removes the animation and sets the property to the specified static value.



#### Examples

For an example, see <a href="/windows/desktop/directcomp/how-to--build-a-visual-tree">How to Build a Simple Visual Tree</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>



<a href="/previous-versions/windows/desktop/legacy/hh449171(v=vs.85)">IDCompositionVisual::SetOffsetY</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
