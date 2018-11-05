---
UID: NF:dcomp.IDCompositionDevice.CreateMatrixTransform
title: IDCompositionDevice::CreateMatrixTransform
author: windows-sdk-content
description: Creates a 2D 3-by-2 matrix transform object.
old-location: directcomp\idcompositiondevice_creatematrixtransform.htm
tech.root: directcomp
ms.assetid: 79291366-2fb2-4130-a642-4993648d8aa6
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateMatrixTransform, CreateMatrixTransform method [DirectComposition], CreateMatrixTransform method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateMatrixTransform method, IDCompositionDevice.CreateMatrixTransform, IDCompositionDevice::CreateMatrixTransform, dcomp/IDCompositionDevice::CreateMatrixTransform, directcomp.idcompositiondevice_creatematrixtransform
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
 - IDCompositionDevice.CreateMatrixTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice::CreateMatrixTransform


## -description


Creates a 2D 3-by-2 matrix transform object.


## -parameters




### -param matrixTransform [out]

Type: <b><a href="https://msdn.microsoft.com/150e33f2-3d76-44a8-b2fe-5a2b4a532c3c">IDCompositionMatrixTransform</a>**</b>

The new matrix transform object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A new matrix transform object has the identity matrix as its initial value. The identity matrix is the 3x2 matrix with ones on the main diagonal and zeros elsewhere, as shown in the following illustration. 

<img alt="Three-by-two identity matrix" src="./images/identity_3x2matrix.png"/>

When an identity transform is applied to an object, it does not change the position, shape, or size of the object. It is similar to the way that multiplying a number by one does not change the number. Any transform other than the identity transform will modify the position, shape, and/or size of objects.




## -see-also




<a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

