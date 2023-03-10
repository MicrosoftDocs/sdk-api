---
UID: NF:dcomp.IDCompositionRectangleClip.SetTopRightRadiusY(IDCompositionAnimation)
title: IDCompositionRectangleClip::SetTopRightRadiusY(IDCompositionAnimation) (dcomp.h)
description: Animates the value of the TopRightRadiusY property of this clip. The TopRightRadiusY property specifies the y radius of the ellipse that rounds the top-right corner of the clip.
helpviewer_keywords: ["IDCompositionRectangleClip interface [DirectComposition]","SetTopRightRadiusY method","IDCompositionRectangleClip.SetTopRightRadiusY","IDCompositionRectangleClip.SetTopRightRadiusY(IDCompositionAnimation)","IDCompositionRectangleClip::SetTopRightRadiusY","IDCompositionRectangleClip::SetTopRightRadiusY(IDCompositionAnimation)","IDCompositionRectangleClip::SetTopRightRadiusY(IDCompositionAnimation*)","SetTopRightRadiusY","SetTopRightRadiusY method [DirectComposition]","SetTopRightRadiusY method [DirectComposition]","IDCompositionRectangleClip interface","dcomp/IDCompositionRectangleClip::SetTopRightRadiusY","directcomp.idcompositionrectangleclip_settoprightradiusy_idcompositionanimation"]
old-location: directcomp\idcompositionrectangleclip_settoprightradiusy_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 933F9687-4EDE-4244-82E2-6DD312464AD7
ms.date: 12/05/2018
ms.keywords: IDCompositionRectangleClip interface [DirectComposition],SetTopRightRadiusY method, IDCompositionRectangleClip.SetTopRightRadiusY, IDCompositionRectangleClip.SetTopRightRadiusY(IDCompositionAnimation), IDCompositionRectangleClip::SetTopRightRadiusY, IDCompositionRectangleClip::SetTopRightRadiusY(IDCompositionAnimation), IDCompositionRectangleClip::SetTopRightRadiusY(IDCompositionAnimation*), SetTopRightRadiusY, SetTopRightRadiusY method [DirectComposition], SetTopRightRadiusY method [DirectComposition],IDCompositionRectangleClip interface, dcomp/IDCompositionRectangleClip::SetTopRightRadiusY, directcomp.idcompositionrectangleclip_settoprightradiusy_idcompositionanimation
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
 - IDCompositionRectangleClip::SetTopRightRadiusY
 - dcomp/IDCompositionRectangleClip::SetTopRightRadiusY
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
 - IDCompositionRectangleClip.SetTopRightRadiusY
---

# IDCompositionRectangleClip::SetTopRightRadiusY(IDCompositionAnimation)


## -description

Animates the value of the TopRightRadiusY property of this clip. The TopRightRadiusY property  specifies the y radius of the ellipse that rounds the top-right corner of the clip.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the y radius changes over time. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the y radius unless this method is called again. If the y radius was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrectangleclip">IDCompositionRectangleClip</a>