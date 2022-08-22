---
UID: NF:dcomp.IDCompositionDevice.CreateRotateTransform
title: IDCompositionDevice::CreateRotateTransform (dcomp.h)
description: Creates a 2D rotation transform object. (IDCompositionDevice.CreateRotateTransform)
helpviewer_keywords: ["CreateRotateTransform","CreateRotateTransform method [DirectComposition]","CreateRotateTransform method [DirectComposition]","IDCompositionDevice interface","IDCompositionDevice interface [DirectComposition]","CreateRotateTransform method","IDCompositionDevice.CreateRotateTransform","IDCompositionDevice::CreateRotateTransform","dcomp/IDCompositionDevice::CreateRotateTransform","directcomp.idcompositiondevice_createrotatetransform"]
old-location: directcomp\idcompositiondevice_createrotatetransform.htm
tech.root: directcomp
ms.assetid: 26a58b2c-1c68-4e38-963c-4df7512347f0
ms.date: 12/05/2018
ms.keywords: CreateRotateTransform, CreateRotateTransform method [DirectComposition], CreateRotateTransform method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateRotateTransform method, IDCompositionDevice.CreateRotateTransform, IDCompositionDevice::CreateRotateTransform, dcomp/IDCompositionDevice::CreateRotateTransform, directcomp.idcompositiondevice_createrotatetransform
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
 - IDCompositionDevice::CreateRotateTransform
 - dcomp/IDCompositionDevice::CreateRotateTransform
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
 - IDCompositionDevice.CreateRotateTransform
---

# IDCompositionDevice::CreateRotateTransform


## -description

Creates a 2D rotation transform object.

## -parameters

### -param rotateTransform [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform">IDCompositionRotateTransform</a>**</b>

The new rotation transform object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A new 2D rotation transform object has a static value of zero for the Angle, CenterX, and CenterY properties.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
