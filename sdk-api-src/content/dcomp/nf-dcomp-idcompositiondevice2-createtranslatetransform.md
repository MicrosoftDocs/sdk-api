---
UID: NF:dcomp.IDCompositionDevice2.CreateTranslateTransform
title: IDCompositionDevice2::CreateTranslateTransform (dcomp.h)
description: Creates a 2D translation transform object.helpviewer_keywords: ["CreateTranslateTransform","CreateTranslateTransform method [DirectComposition]","CreateTranslateTransform method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateTranslateTransform method","IDCompositionDevice2.CreateTranslateTransform","IDCompositionDevice2::CreateTranslateTransform","dcomp/IDCompositionDevice2::CreateTranslateTransform","directcomp.idcompositiondevice2_createtranslatetransform"]
old-location: directcomp\idcompositiondevice2_createtranslatetransform.htm
tech.root: directcomp
ms.assetid: 83800B10-7992-4A3D-B8D6-6872BAEAF7DA
ms.date: 12/05/2018
ms.keywords: CreateTranslateTransform, CreateTranslateTransform method [DirectComposition], CreateTranslateTransform method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateTranslateTransform method, IDCompositionDevice2.CreateTranslateTransform, IDCompositionDevice2::CreateTranslateTransform, dcomp/IDCompositionDevice2::CreateTranslateTransform, directcomp.idcompositiondevice2_createtranslatetransform
f1_keywords:
- dcomp/IDCompositionDevice2.CreateTranslateTransform
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
- IDCompositionDevice2.CreateTranslateTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDevice2::CreateTranslateTransform


## -description


Creates a 2D translation transform object.


## -parameters




### -param translateTransform [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontranslatetransform">IDCompositionTranslateTransform</a>**</b>

The new 2D translation transform object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A new 2D translation transform object has a static value of zero for the OffsetX and OffsetY properties.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
 

 

