---
UID: NF:dcomp.IDCompositionVisual.SetClip(constD2D_RECT_F&)
title: IDCompositionVisual::SetClip (dcomp.h)
description: Sets the Clip property of this visual to the specified rectangle.
helpviewer_keywords: ["IDCompositionVisual interface [DirectComposition]","SetClip method","IDCompositionVisual.SetClip","IDCompositionVisual::SetClip","IDCompositionVisual::SetClip(const D2D_RECT_F &)","IDCompositionVisual::SetClip(const D2D_RECT_F&)","SetClip","SetClip method [DirectComposition]","SetClip method [DirectComposition]","IDCompositionVisual interface","dcomp/IDCompositionVisual::SetClip","directcomp.idcompositionvisual_setclip_const_d2d_rect_f_"]
old-location: directcomp\idcompositionvisual_setclip_const_d2d_rect_f_.htm
tech.root: directcomp
ms.assetid: 7F01EB25-3A44-416F-A926-D185F2FD44EC
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetClip method, IDCompositionVisual.SetClip, IDCompositionVisual::SetClip, IDCompositionVisual::SetClip(const D2D_RECT_F &), IDCompositionVisual::SetClip(const D2D_RECT_F&), SetClip, SetClip method [DirectComposition], SetClip method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetClip, directcomp.idcompositionvisual_setclip_const_d2d_rect_f_
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
 - IDCompositionVisual::SetClip
 - dcomp/IDCompositionVisual::SetClip
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
 - IDCompositionVisual.SetClip
---

# IDCompositionVisual::SetClip


## -description

Sets the Clip property of this visual to the specified rectangle. The Clip property restricts the rendering of the 
        visual subtree that is rooted at this visual to the specified rectangular region.

## -parameters

### -param rect [in, ref]

Type: <b>const <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f">D2D_RECT_F</a></b>

The rectangle to use to clip this visual. All properties of the rect parameter have a numerical limit of -2^21 to 2^21. 
          The API accepts numbers outside of this range, but they are always clamped to this range.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. 
              See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

Setting the Clip property clips this visual along with all visuals in the subtree that is rooted at this visual. The clip is transformed by the OffsetX, OffsetY, and Transform properties. 

If the Clip property previously specified a clip object, the newly specified clip rectangle replaces the clip object.

This method fails if any members of the <i>rect</i> structure are NaN, positive infinity, or negative infinity.

      

If the clip rectangle is empty, the visual is fully clipped; that is, the visual is included in the visual tree, but it does not render anything. 
      To exclude a particular visual from a composition, remove the visual from the visual tree instead of setting an empty clip rectangle. 
      Removing the visual results in better performance.

## -see-also

<a href="/windows/desktop/directcomp/clipping">Clipping</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrectangleclip">IDCompositionRectangleClip</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>