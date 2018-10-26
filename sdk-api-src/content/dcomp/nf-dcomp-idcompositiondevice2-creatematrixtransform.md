---
UID: NF:dcomp.IDCompositionDevice2.CreateMatrixTransform
title: IDCompositionDevice2::CreateMatrixTransform
author: windows-sdk-content
description: Creates a 2D 3-by-2 matrix transform object.
old-location: directcomp\idcompositiondevice2_creatematrixtransform.htm
tech.root: directcomp
ms.assetid: 4E8D8560-F7D3-4075-A4E9-00AFCEB526BE
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CreateMatrixTransform, CreateMatrixTransform method [DirectComposition], CreateMatrixTransform method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateMatrixTransform method, IDCompositionDevice2.CreateMatrixTransform, IDCompositionDevice2::CreateMatrixTransform, dcomp/IDCompositionDevice2::CreateMatrixTransform, directcomp.idcompositiondevice2_creatematrixtransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDCompositionDevice2.CreateMatrixTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice2::CreateMatrixTransform


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

<img alt="Three-by-two identity matrix" src="images/identity_3x2matrix.png"/>

When an identity transform is applied to an object, it does not change the position, shape, or size of the object. It is similar to the way that multiplying a number by one does not change the number. Any transform other than the identity transform will modify the position, shape, and/or size of objects.




## -see-also




<a href="https://msdn.microsoft.com/0E5D0AEC-63A3-4A44-9A0B-D1E26789CAB0">IDCompositionDevice2</a>



<a href="https://msdn.microsoft.com/40935581-D45C-496B-90B9-152963F0B55A">IDCompositionEffectGroup::SetTransform3D</a>



<a href="https://msdn.microsoft.com/CCA785F6-869C-460A-AF54-573BDE798685">IDCompositionVisual::SetEffect</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

