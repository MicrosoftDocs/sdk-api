---
UID: NF:dcomp.IDCompositionVisual.SetTransform(IDCompositionTransform)
title: IDCompositionVisual::SetTransform(IDCompositionTransform) (dcomp.h)
description: Sets the Transform property of this visual to the specified 2D transform object.
helpviewer_keywords: ["IDCompositionVisual interface [DirectComposition]","SetTransform method","IDCompositionVisual.SetTransform","IDCompositionVisual.SetTransform(IDCompositionTransform)","IDCompositionVisual::SetTransform","IDCompositionVisual::SetTransform(IDCompositionTransform)","IDCompositionVisual::SetTransform(IDCompositionTransform*)","SetTransform","SetTransform method [DirectComposition]","SetTransform method [DirectComposition]","IDCompositionVisual interface","dcomp/IDCompositionVisual::SetTransform","directcomp.idcompositionvisual_settransform_idcompositiontransform"]
old-location: directcomp\idcompositionvisual_settransform_idcompositiontransform.htm
tech.root: directcomp
ms.assetid: 448B853E-B045-4D06-BCC8-E1578E36C20A
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetTransform method, IDCompositionVisual.SetTransform, IDCompositionVisual.SetTransform(IDCompositionTransform), IDCompositionVisual::SetTransform, IDCompositionVisual::SetTransform(IDCompositionTransform), IDCompositionVisual::SetTransform(IDCompositionTransform*), SetTransform, SetTransform method [DirectComposition], SetTransform method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetTransform, directcomp.idcompositionvisual_settransform_idcompositiontransform
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
 - IDCompositionVisual::SetTransform
 - dcomp/IDCompositionVisual::SetTransform
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
 - IDCompositionVisual.SetTransform
---

# IDCompositionVisual::SetTransform(IDCompositionTransform)


## -description

Sets the Transform property of this visual to the specified 2D transform object.

## -parameters

### -param transform [in, optional]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>*</b>

The transform object that is used to modify  the coordinate system of this visual. This parameter can point to an <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a> interface or one of its derived interfaces. This parameter can be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

Setting the Transform property transforms the coordinate system of the entire visual subtree that is rooted at this visual. If the Clip property of this visual is specified, the clip rectangle is also transformed.



If the Transform property previously specified a transform matrix, the newly specified transform object replaces the transform matrix.

A transformation specified by the Transform property is applied after the OffsetX and OffsetY properties. In other words, the effect of setting the Transform property and the OffsetX and OffsetY properties is the same as setting only the Transform property on a transform group where the first member of the group is an <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform">IDCompositionTranslateTransform</a> object that has those same OffsetX and OffsetY values. However, you should use the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setoffsetx(float)">IDCompositionVisual::SetOffsetX</a> and <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setoffsety(idcompositionanimation)">SetOffsetY</a> methods whenever possible because they are slightly faster. 

This method fails if <i>transform</i> is an invalid pointer or if it was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface that created this visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.


If the <i>transform</i> parameter is NULL, the coordinate system of this visual is transformed only by its OffsetX and OffsetY properties. Setting the Transform property to NULL is equivalent to setting it to an <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionmatrixtransform">IDCompositionMatrixTransform</a> object where the specified matrix is the identity matrix. However, an application should set the Transform property to NULL whenever possible because it is slightly faster.

If the OffsetX and OffsetY properties are set to 0, and the Transform property is set to NULL, the coordinate system of the visual is the same as that of its parent.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionmatrixtransform">IDCompositionMatrixTransform</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform">IDCompositionRotateTransform</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform">IDCompositionScaleTransform</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionskewtransform">IDCompositionSkewTransform</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform">IDCompositionTranslateTransform</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>



<a href="/previous-versions/windows/desktop/legacy/hh449165(v=vs.85)">IDCompositionVisual::SetOffsetX</a>



<a href="/previous-versions/windows/desktop/legacy/hh449171(v=vs.85)">IDCompositionVisual::SetOffsetY</a>