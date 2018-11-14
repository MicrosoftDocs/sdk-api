---
UID: NF:dcomp.IDCompositionAffineTransform2DEffect.SetTransformMatrixElement(int,int,IDCompositionAnimation)
title: IDCompositionAffineTransform2DEffect::SetTransformMatrixElement(int,int,IDCompositionAnimation)
author: windows-sdk-content
description: Sets an element of the transform matrix of the effect.
old-location: directcomp\idcompositionaffinetransform2deffect_settransformmatrixelement_2.htm
tech.root: directcomp
ms.assetid: 7BD6F43D-4E3B-4D50-BB9C-FAF27E9B50C1
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDCompositionAffineTransform2DEffect interface [DirectComposition],SetTransformMatrixElement method, IDCompositionAffineTransform2DEffect.SetTransformMatrixElement, IDCompositionAffineTransform2DEffect.SetTransformMatrixElement(int,int,IDCompositionAnimation), IDCompositionAffineTransform2DEffect::SetTransformMatrixElement, IDCompositionAffineTransform2DEffect::SetTransformMatrixElement(int,int,IDCompositionAnimation), SetTransformMatrixElement, SetTransformMatrixElement method [DirectComposition], SetTransformMatrixElement method [DirectComposition],IDCompositionAffineTransform2DEffect interface, dcomp/IDCompositionAffineTransform2DEffect::SetTransformMatrixElement, directcomp.idcompositionaffinetransform2deffect_settransformmatrixelement_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDCompositionAffineTransform2DEffect.SetTransformMatrixElement
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
- IDCompositionAffineTransform2DEffect.SetTransformMatrixElement
: 
---

# IDCompositionAffineTransform2DEffect::SetTransformMatrixElement(int,int,IDCompositionAnimation)


## -description


Sets an element of the transform matrix of the effect.


## -parameters




### -param row [in]

Type: <b>int</b>

The row of the element.


### -param column [in]

Type: <b>int</b>

The columen of the element.


### -param animation [in]

Type: <b><a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>*</b>

An animation that represents how the element value changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1B693705-1118-4B9B-A7B7-E8811AE881AC">IDCompositionAffineTransform2DEffect</a>
 

 

