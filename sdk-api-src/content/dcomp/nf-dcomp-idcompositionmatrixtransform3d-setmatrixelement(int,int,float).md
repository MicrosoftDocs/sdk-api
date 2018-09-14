---
UID: NF:dcomp.IDCompositionMatrixTransform3D.SetMatrixElement(int,int,float)
title: IDCompositionMatrixTransform3D::SetMatrixElement(int,int,float)
author: windows-sdk-content
description: Changes the value of one element of the matrix of this 3D transform.
old-location: directcomp\idcompositionmatrixtransform3d_setmatrixelement_float.htm
tech.root: directcomp
ms.assetid: 5AB88C3B-7901-413E-929A-8A80EDD8962F
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDCompositionMatrixTransform3D interface [DirectComposition],SetMatrixElement method, IDCompositionMatrixTransform3D.SetMatrixElement, IDCompositionMatrixTransform3D.SetMatrixElement(int,int,float), IDCompositionMatrixTransform3D::SetMatrixElement, IDCompositionMatrixTransform3D::SetMatrixElement(int,int,float), SetMatrixElement, SetMatrixElement method [DirectComposition], SetMatrixElement method [DirectComposition],IDCompositionMatrixTransform3D interface, dcomp/IDCompositionMatrixTransform3D::SetMatrixElement, directcomp.idcompositionmatrixtransform3d_setmatrixelement_float
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
 - IDCompositionMatrixTransform3D.SetMatrixElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionMatrixTransform3D::SetMatrixElement(int,int,float)


## -description


Changes the value of one element of the matrix of this 3D transform.


## -parameters




### -param row [in]

Type: <b>int</b>

The row index of the element to change. This value must be between 0 and 3, inclusive.


### -param column [in]

Type: <b>int</b>

The column index of the element to change. This value must be between 0 and 3, inclusive.


### -param value [in]

Type: <b>float</b>

The new value of the specified element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>value</i> parameter is NaN, positive infinity, or negative infinity.

If the specified element was previously animated, this method removes the animation and sets the element to the specified static value.




## -see-also




<a href="https://msdn.microsoft.com/56C9A564-2504-4940-B850-D280C8E0CF82">IDCompositionMatrixTransform3D</a>
 

 

