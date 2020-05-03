---
UID: NF:dcomp.IDCompositionDevice.CreateTranslateTransform
title: IDCompositionDevice::CreateTranslateTransform (dcomp.h)
description: Creates a 2D translation transform object.helpviewer_keywords: ["CreateTranslateTransform","CreateTranslateTransform method [DirectComposition]","CreateTranslateTransform method [DirectComposition]","IDCompositionDevice interface","IDCompositionDevice interface [DirectComposition]","CreateTranslateTransform method","IDCompositionDevice.CreateTranslateTransform","IDCompositionDevice::CreateTranslateTransform","dcomp/IDCompositionDevice::CreateTranslateTransform","directcomp.idcompositiondevice_createtranslatetransform"]
old-location: directcomp\idcompositiondevice_createtranslatetransform.htm
tech.root: directcomp
ms.assetid: 15b16ff7-cf7e-455e-beb7-737f2cc21f9d
ms.date: 12/05/2018
ms.keywords: CreateTranslateTransform, CreateTranslateTransform method [DirectComposition], CreateTranslateTransform method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateTranslateTransform method, IDCompositionDevice.CreateTranslateTransform, IDCompositionDevice::CreateTranslateTransform, dcomp/IDCompositionDevice::CreateTranslateTransform, directcomp.idcompositiondevice_createtranslatetransform
f1_keywords:
- dcomp/IDCompositionDevice.CreateTranslateTransform
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
- IDCompositionDevice.CreateTranslateTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDevice::CreateTranslateTransform


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




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
 

 

