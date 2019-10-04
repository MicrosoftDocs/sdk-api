---
UID: NF:dcomp.IDCompositionDevice.CreateScaleTransform3D
title: IDCompositionDevice::CreateScaleTransform3D (dcomp.h)
author: windows-sdk-content
description: Creates a 3D scale transform object.
old-location: directcomp\idcompositiondevice_createscaletransform3d.htm
tech.root: directcomp
ms.assetid: 6B9AEEB9-559A-4B7B-A4B5-1C976B92BE7B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateScaleTransform3D, CreateScaleTransform3D method [DirectComposition], CreateScaleTransform3D method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateScaleTransform3D method, IDCompositionDevice.CreateScaleTransform3D, IDCompositionDevice::CreateScaleTransform3D, dcomp/IDCompositionDevice::CreateScaleTransform3D, directcomp.idcompositiondevice_createscaletransform3d
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionDevice.CreateScaleTransform3D"
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
 - IDCompositionDevice.CreateScaleTransform3D
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDevice::CreateScaleTransform3D


## -description


Creates a 3D scale transform object.


## -parameters




### -param scaleTransform3D [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionscaletransform3d">IDCompositionScaleTransform3D</a>**</b>

The new 3D scale transform object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A new 3D scale transform object has a static value of 1.0 for the ScaleX, ScaleY, and ScaleZ properties.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositioneffectgroup-settransform3d">IDCompositionEffectGroup::SetTransform3D</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>
 

 

