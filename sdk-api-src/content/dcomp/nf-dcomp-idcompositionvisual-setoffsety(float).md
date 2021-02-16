---
UID: NF:dcomp.IDCompositionVisual.SetOffsetY(float)
title: IDCompositionVisual::SetOffsetY (dcomp.h)
description: Changes the value of the OffsetY property of this visual.
helpviewer_keywords: ["IDCompositionVisual interface [DirectComposition]","SetOffsetY method","IDCompositionVisual.SetOffsetY","IDCompositionVisual::SetOffsetY","IDCompositionVisual::SetOffsetY(float)","SetOffsetY","SetOffsetY method [DirectComposition]","SetOffsetY method [DirectComposition]","IDCompositionVisual interface","dcomp/IDCompositionVisual::SetOffsetY","directcomp.idcompositionvisual_setoffsety_float"]
old-location: directcomp\idcompositionvisual_setoffsety_float.htm
tech.root: directcomp
ms.assetid: 7FF2433A-1741-4177-85C8-F5AE0D920EB4
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetOffsetY method, IDCompositionVisual.SetOffsetY, IDCompositionVisual::SetOffsetY, IDCompositionVisual::SetOffsetY(float), SetOffsetY, SetOffsetY method [DirectComposition], SetOffsetY method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetOffsetY, directcomp.idcompositionvisual_setoffsety_float
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
 - IDCompositionVisual::SetOffsetY
 - dcomp/IDCompositionVisual::SetOffsetY
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
 - IDCompositionVisual.SetOffsetY
---

# IDCompositionVisual::SetOffsetY


## -description

Changes the value of the OffsetY property of this visual.  The OffsetY property specifies the new offset of the visual along the y-axis, relative to the parent visual.

## -parameters

### -param offsetY [in]

Type: <b>float</b>

The new offset of the visual along the y-axis, in pixels.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method fails if the <i>offsetY</i> parameter is NaN, positive infinity, or negative infinity.



Changing the OffsetY property transforms the coordinate system of the entire visual subtree that is rooted at this visual. If the Clip property of this visual is specified, the clip rectangle is also transformed.



A transformation that is specified by the Transform property is applied after the OffsetY property.  In other words, the effect of setting the Transform property and the OffsetY property is the same as setting only the Transform property on a transform group object where the first member of the group is an <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform">IDCompositionTranslateTransform</a> object that has the same OffsetY value as <i>offsetY</i>. However, you should use  <b>IDCompositionVisual::SetOffsetY</b> whenever possible because it is slightly faster.

If the OffsetX and OffsetY properties are set to 0, and the Transform property is set to NULL, the coordinate system of the visual is the same as that of its parent.

If the OffsetY property was previously animated, this method removes the animation and sets the property to the specified static value.



#### Examples

For an example, see <a href="/windows/desktop/directcomp/how-to--build-a-visual-tree">How to Build a Simple Visual Tree</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>



<a href="/previous-versions/windows/desktop/legacy/hh449165(v=vs.85)">IDCompositionVisual::SetOffsetX</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>