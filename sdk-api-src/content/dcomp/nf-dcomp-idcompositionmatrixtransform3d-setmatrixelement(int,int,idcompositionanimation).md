---
UID: NF:dcomp.IDCompositionMatrixTransform3D.SetMatrixElement(int,int,IDCompositionAnimation)
title: IDCompositionMatrixTransform3D::SetMatrixElement(int,int,IDCompositionAnimation)
author: windows-sdk-content
description: Animates the value of one element of the matrix of this 3D transform.
old-location: directcomp\idcompositionmatrixtransform3d_setmatrixelement_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 099AB3AB-D0F8-4D25-B407-83C77810F34D
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDCompositionMatrixTransform3D interface [DirectComposition],SetMatrixElement method, IDCompositionMatrixTransform3D.SetMatrixElement, IDCompositionMatrixTransform3D.SetMatrixElement(int,int,IDCompositionAnimation), IDCompositionMatrixTransform3D::SetMatrixElement, IDCompositionMatrixTransform3D::SetMatrixElement(int,int,IDCompositionAnimation), IDCompositionMatrixTransform3D::SetMatrixElement(int,int,IDCompositionAnimation*), SetMatrixElement, SetMatrixElement method [DirectComposition], SetMatrixElement method [DirectComposition],IDCompositionMatrixTransform3D interface, dcomp/IDCompositionMatrixTransform3D::SetMatrixElement, directcomp.idcompositionmatrixtransform3d_setmatrixelement_idcompositionanimation
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
- apiref
: 
- COM
: 
- dcomp.h
: 
- IDCompositionMatrixTransform3D.SetMatrixElement
: 
---

# IDCompositionMatrixTransform3D::SetMatrixElement(int,int,IDCompositionAnimation)


## -description


Animates the value of one element of the matrix of this 3D transform.


## -parameters




### -param row [in]

Type: <b>int</b>

The row index of the element to change. This value must be between 0 and 3, inclusive.


### -param column [in]

Type: <b>int</b>

The column index of the element to change. This value must be between 0 and 3, inclusive.


### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation that represents how the value of the specified element changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the specified element unless this method is called again. If the specified element was previously animated, calling this method replaces the previous animation with the new animation.

This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a> interface as the affected transform. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.




## -see-also




<a href="https://msdn.microsoft.com/56C9A564-2504-4940-B850-D280C8E0CF82">IDCompositionMatrixTransform3D</a>
 

 

