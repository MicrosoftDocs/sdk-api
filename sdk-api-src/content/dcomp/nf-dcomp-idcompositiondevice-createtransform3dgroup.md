---
UID: NF:dcomp.IDCompositionDevice.CreateTransform3DGroup
title: IDCompositionDevice::CreateTransform3DGroup (dcomp.h)
description: The IDCompositionDevice::CreateTransform3DGroup method creates a 3D transform group object that holds an array of 3D transform objects.
helpviewer_keywords: ["CreateTransform3DGroup","CreateTransform3DGroup method [DirectComposition]","CreateTransform3DGroup method [DirectComposition]","IDCompositionDevice interface","IDCompositionDevice interface [DirectComposition]","CreateTransform3DGroup method","IDCompositionDevice.CreateTransform3DGroup","IDCompositionDevice::CreateTransform3DGroup","dcomp/IDCompositionDevice::CreateTransform3DGroup","directcomp.idcompositiondevice_createtransform3dgroup"]
old-location: directcomp\idcompositiondevice_createtransform3dgroup.htm
tech.root: directcomp
ms.assetid: 47119ECA-CAA0-41E7-821E-18E99B6C91BD
ms.date: 06/23/2022
ms.keywords: CreateTransform3DGroup, CreateTransform3DGroup method [DirectComposition], CreateTransform3DGroup method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateTransform3DGroup method, IDCompositionDevice.CreateTransform3DGroup, IDCompositionDevice::CreateTransform3DGroup, dcomp/IDCompositionDevice::CreateTransform3DGroup, directcomp.idcompositiondevice_createtransform3dgroup
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
 - IDCompositionDevice::CreateTransform3DGroup
 - dcomp/IDCompositionDevice::CreateTransform3DGroup
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
 - IDCompositionDevice.CreateTransform3DGroup
---

# IDCompositionDevice::CreateTransform3DGroup


## -description

Creates a 3D transform group object that holds an array of 3D transform objects.

## -parameters

### -param transforms3D [in]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>**</b>

An array of 3D transform objects that make up this transform group.

### -param elements [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of elements in the <i>transforms</i> array.

### -param transform3DGroup [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform3d">IDCompositionTransform3D</a>**</b>

The new 3D transform group object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

The array entries in a 3D transform group cannot be changed. However, each transform in the array can be modified through its own property setting methods. If a transform in the array is modified, the change is reflected in the computed matrix of the transform group.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d">IDCompositionEffectGroup::SetTransform3D</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>