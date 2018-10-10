---
UID: NF:dcomp.IDCompositionMatrixTransform3D.SetMatrix
title: IDCompositionMatrixTransform3D::SetMatrix
author: windows-sdk-content
description: Changes all values of the matrix of this 3D transformation effect.
old-location: directcomp\idcompositionmatrixtransform3d_setmatrix.htm
tech.root: directcomp
ms.assetid: 0F1DBC1C-154A-4785-B9B9-924353FD5836
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IDCompositionMatrixTransform3D interface [DirectComposition],SetMatrix method, IDCompositionMatrixTransform3D.SetMatrix, IDCompositionMatrixTransform3D::SetMatrix, SetMatrix, SetMatrix method [DirectComposition], SetMatrix method [DirectComposition],IDCompositionMatrixTransform3D interface, dcomp/IDCompositionMatrixTransform3D::SetMatrix, directcomp.idcompositionmatrixtransform3d_setmatrix
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
 - IDCompositionMatrixTransform3D.SetMatrix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionMatrixTransform3D::SetMatrix


## -description


Changes all values of the matrix of this 3D transformation effect.


## -parameters




### -param matrix [ref]

Type: <b>const <a href="https://msdn.microsoft.com/d6b98a32-e745-4724-b8ce-a81a3f5416f3">D3DMATRIX</a></b>

The new matrix for this 3D transformation effect.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if any of the matrix values are NaN, positive infinity, or negative infinity.

If any of the matrix elements were previously animated, this method removes the animations and sets the elements to the specified static value.




## -see-also




<a href="https://msdn.microsoft.com/56C9A564-2504-4940-B850-D280C8E0CF82">IDCompositionMatrixTransform3D</a>
 

 

