---
UID: NF:dcomp.IDCompositionVisual.SetOffsetX(IDCompositionAnimation)
title: IDCompositionVisual::SetOffsetX(IDCompositionAnimation) (dcomp.h)
author: windows-sdk-content
description: Changes the value of the OffsetX property of this visual.
old-location: directcomp\idcompositionvisual_setoffsetx_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: f0595951-a0b0-47bb-9e94-1cbaa7b7f736
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetOffsetX method, IDCompositionVisual.SetOffsetX, IDCompositionVisual.SetOffsetX(IDCompositionAnimation), IDCompositionVisual::SetOffsetX, IDCompositionVisual::SetOffsetX(IDCompositionAnimation), IDCompositionVisual::SetOffsetX(IDCompositionAnimation*), SetOffsetX, SetOffsetX method [DirectComposition], SetOffsetX method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetOffsetX, directcomp.idcompositionvisual_setoffsetx_idcompositionanimation
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionVisual.SetOffsetX"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionVisual.SetOffsetX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionVisual::SetOffsetX(IDCompositionAnimation)


## -description


Changes the value of the OffsetX property of this visual.  The OffsetX property specifies the new offset of the visual along the x-axis, relative to the parent visual.


## -parameters




### -param animation [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the OffsetX property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the animation object referenced by the <i>animation</i> parameter is changed after this call, the change does not affect the OffsetX property unless this method is called again. If the OffsetX property was previously animated, this method replaces that animation with the new animation.

This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface that created this visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449171(v=vs.85)">IDCompositionVisual::SetOffsetY</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
 

 

