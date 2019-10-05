---
UID: NF:dcomp.IDCompositionRotateTransform.SetCenterY(IDCompositionAnimation)
title: IDCompositionRotateTransform::SetCenterY(IDCompositionAnimation) (dcomp.h)
author: windows-sdk-content
description: Animates the value of the CenterY property of a 2D rotation transform.
old-location: directcomp\idcompositionrotatetransform_setcentery_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: AD53EEF7-4DCE-4B6D-9A72-010033958155
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionRotateTransform interface [DirectComposition],SetCenterY method, IDCompositionRotateTransform.SetCenterY, IDCompositionRotateTransform.SetCenterY(IDCompositionAnimation), IDCompositionRotateTransform::SetCenterY, IDCompositionRotateTransform::SetCenterY(IDCompositionAnimation), IDCompositionRotateTransform::SetCenterY(IDCompositionAnimation*), SetCenterY, SetCenterY method [DirectComposition], SetCenterY method [DirectComposition],IDCompositionRotateTransform interface, dcomp/IDCompositionRotateTransform::SetCenterY, directcomp.idcompositionrotatetransform_setcentery_idcompositionanimation
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionRotateTransform.SetCenterY"
dev_langs:
 - c++
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
 - IDCompositionRotateTransform.SetCenterY
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionRotateTransform::SetCenterY(IDCompositionAnimation)


## -description


Animates the value of the CenterY property of a 2D rotation transform. The CenterY property specifies the y-coordinate of the point about which the rotation is performed.


## -parameters




### -param animation [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation object that determines how the value of the CenterY property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the CenterY property unless this method is called again. If the CenterY property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform">IDCompositionRotateTransform</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh448982(v=vs.85)">IDCompositionRotateTransform::SetCenterX</a>
 

 

