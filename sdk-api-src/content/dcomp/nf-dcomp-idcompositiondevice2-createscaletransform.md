---
UID: NF:dcomp.IDCompositionDevice2.CreateScaleTransform
title: IDCompositionDevice2::CreateScaleTransform (dcomp.h)
description: Creates a 2D scale transform object.
helpviewer_keywords: ["CreateScaleTransform","CreateScaleTransform method [DirectComposition]","CreateScaleTransform method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateScaleTransform method","IDCompositionDevice2.CreateScaleTransform","IDCompositionDevice2::CreateScaleTransform","dcomp/IDCompositionDevice2::CreateScaleTransform","directcomp.idcompositiondevice2_createscaletransform"]
old-location: directcomp\idcompositiondevice2_createscaletransform.htm
tech.root: directcomp
ms.assetid: 800BA1EF-C801-4E93-BBA0-6C8FD0ACCB68
ms.date: 12/05/2018
ms.keywords: CreateScaleTransform, CreateScaleTransform method [DirectComposition], CreateScaleTransform method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateScaleTransform method, IDCompositionDevice2.CreateScaleTransform, IDCompositionDevice2::CreateScaleTransform, dcomp/IDCompositionDevice2::CreateScaleTransform, directcomp.idcompositiondevice2_createscaletransform
f1_keywords:
- dcomp/IDCompositionDevice2.CreateScaleTransform
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
- IDCompositionDevice2.CreateScaleTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDevice2::CreateScaleTransform


## -description


Creates a 2D scale transform object.


## -parameters




### -param scaleTransform [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform">IDCompositionScaleTransform</a>**</b>

The new 2D scale transform object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A new 2D scale transform object has a static value of zero for the ScaleX, ScaleY, CenterX, and CenterY properties.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
 

 

