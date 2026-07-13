---
UID: NF:dcomp.IDCompositionDevice.CreateRotateTransform3D
title: IDCompositionDevice::CreateRotateTransform3D (dcomp.h)
description: The CreateRotateTransform3D method in the IDCompositionDevice interface creates a 3D rotation transform object.
helpviewer_keywords: ["CreateRotateTransform3D","CreateRotateTransform3D method [DirectComposition]","CreateRotateTransform3D method [DirectComposition]","IDCompositionDevice interface","IDCompositionDevice interface [DirectComposition]","CreateRotateTransform3D method","IDCompositionDevice.CreateRotateTransform3D","IDCompositionDevice::CreateRotateTransform3D","dcomp/IDCompositionDevice::CreateRotateTransform3D","directcomp.idcompositiondevice_createrotatetransform3d"]
old-location: directcomp\idcompositiondevice_createrotatetransform3d.htm
tech.root: directcomp
ms.assetid: 0F680BDB-F845-42AD-8888-B0E4A106D9CB
ms.date: 06/23/2022
ms.keywords: CreateRotateTransform3D, CreateRotateTransform3D method [DirectComposition], CreateRotateTransform3D method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateRotateTransform3D method, IDCompositionDevice.CreateRotateTransform3D, IDCompositionDevice::CreateRotateTransform3D, dcomp/IDCompositionDevice::CreateRotateTransform3D, directcomp.idcompositiondevice_createrotatetransform3d
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
 - IDCompositionDevice::CreateRotateTransform3D
 - dcomp/IDCompositionDevice::CreateRotateTransform3D
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
 - IDCompositionDevice.CreateRotateTransform3D
---

# IDCompositionDevice::CreateRotateTransform3D


## -description

Creates a 3D rotation transform object.

## -parameters

### -param rotateTransform3D [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrotatetransform3d">IDCompositionRotateTransform3D</a>**</b>

The new 3D rotation transform object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A new 3D rotation transform object has a default static value of zero for the Angle, CenterX, CenterY, AxisX, and AxisY properties, and a default static value of 1.0 for the AxisZ property.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionEffectGroup::SetTransform</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>