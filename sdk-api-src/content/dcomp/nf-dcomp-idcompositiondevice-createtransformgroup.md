---
UID: NF:dcomp.IDCompositionDevice.CreateTransformGroup
title: IDCompositionDevice::CreateTransformGroup (dcomp.h)
description: Creates a 2D transform group object that holds an array of 2D transform objects.
old-location: directcomp\idcompositiondevice_createtransformgroup.htm
tech.root: directcomp
ms.assetid: 9d080bd1-f8ea-4a86-89bc-f4a801917335
ms.date: 12/05/2018
ms.keywords: CreateTransformGroup, CreateTransformGroup method [DirectComposition], CreateTransformGroup method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateTransformGroup method, IDCompositionDevice.CreateTransformGroup, IDCompositionDevice::CreateTransformGroup, dcomp/IDCompositionDevice::CreateTransformGroup, directcomp.idcompositiondevice_createtransformgroup
f1_keywords:
- dcomp/IDCompositionDevice.CreateTransformGroup
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
- IDCompositionDevice.CreateTransformGroup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDevice::CreateTransformGroup


## -description


Creates a 2D transform group object that holds an array of 2D transform objects.


## -parameters




### -param transforms [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>**</b>

An array of 2D transform objects that make up this transform group.


### -param elements [in]

Type: <b>UINT</b>

The number of elements in the <i>transforms</i> array.


### -param transformGroup [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiontransform">IDCompositionTransform</a>**</b>

The new transform group object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



The array entries in a transform group cannot be changed. However, each transform in the array can be modified through its own property setting methods. If a transform in the array is modified, the change is reflected in the computed matrix of the transform group.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
 

 

