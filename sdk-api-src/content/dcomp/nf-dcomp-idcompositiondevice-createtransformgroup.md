---
UID: NF:dcomp.IDCompositionDevice.CreateTransformGroup
title: IDCompositionDevice::CreateTransformGroup
author: windows-sdk-content
description: Creates a 2D transform group object that holds an array of 2D transform objects.
old-location: directcomp\idcompositiondevice_createtransformgroup.htm
tech.root: directcomp
ms.assetid: 9d080bd1-f8ea-4a86-89bc-f4a801917335
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CreateTransformGroup, CreateTransformGroup method [DirectComposition], CreateTransformGroup method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateTransformGroup method, IDCompositionDevice.CreateTransformGroup, IDCompositionDevice::CreateTransformGroup, dcomp/IDCompositionDevice::CreateTransformGroup, directcomp.idcompositiondevice_createtransformgroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice::CreateTransformGroup


## -description


Creates a 2D transform group object that holds an array of 2D transform objects.


## -parameters




### -param transforms [in]

Type: <b><a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>**</b>

An array of 2D transform objects that make up this transform group.


### -param elements [in]

Type: <b>UINT</b>

The number of elements in the <i>transforms</i> array.


### -param transformGroup [out]

Type: <b><a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>**</b>

The new transform group object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



The array entries in a transform group cannot be changed. However, each transform in the array can be modified through its own property setting methods. If a transform in the array is modified, the change is reflected in the computed matrix of the transform group.




## -see-also




<a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

