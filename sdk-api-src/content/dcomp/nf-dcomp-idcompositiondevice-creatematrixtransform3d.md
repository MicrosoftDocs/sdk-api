---
UID: NF:dcomp.IDCompositionDevice.CreateMatrixTransform3D
title: IDCompositionDevice::CreateMatrixTransform3D
author: windows-sdk-content
description: Creates a 3D 4-by-4 matrix transform object.
old-location: directcomp\idcompositiondevice_creatematrixtransform3d.htm
tech.root: directcomp
ms.assetid: 699DB053-3897-43EC-92E2-BD45CE643130
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateMatrixTransform3D, CreateMatrixTransform3D method [DirectComposition], CreateMatrixTransform3D method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateMatrixTransform3D method, IDCompositionDevice.CreateMatrixTransform3D, IDCompositionDevice::CreateMatrixTransform3D, dcomp/IDCompositionDevice::CreateMatrixTransform3D, directcomp.idcompositiondevice_creatematrixtransform3d
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
 - IDCompositionDevice.CreateMatrixTransform3D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice::CreateMatrixTransform3D


## -description


Creates a 3D 4-by-4 matrix transform object.


## -parameters




### -param matrixTransform3D [out]

Type: <b><a href="https://msdn.microsoft.com/56C9A564-2504-4940-B850-D280C8E0CF82">IDCompositionMatrixTransform3D</a>**</b>

The new 3D matrix transform object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



The new 3D matrix transform has the identity matrix as its value. The identity matrix is the 4-by-4 matrix with ones on the main diagonal and zeros elsewhere, as shown in the following illustration. 

<img alt="Four-by-four identity matrix" src="./images/identity_4x4matrix.png"/>

When an identity transform is applied to an object, it does not change the position, shape, or size of the object. It is similar to the way that multiplying a number by one does not change the number. Any transform other than the identity transform will modify the position, shape, and/or size of objects.




## -see-also




<a href="https://msdn.microsoft.com/40935581-D45C-496B-90B9-152963F0B55A">DCompositionEffectGroup::SetTransform3D</a>



<a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a>
 

 

