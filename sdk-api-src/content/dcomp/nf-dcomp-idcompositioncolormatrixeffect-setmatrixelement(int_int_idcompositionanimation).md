---
UID: NF:dcomp.IDCompositionColorMatrixEffect.SetMatrixElement(int,int,IDCompositionAnimation)
title: IDCompositionColorMatrixEffect::SetMatrixElement(int,int,IDCompositionAnimation) (dcomp.h)
description: Sets an element of the color matrix.
helpviewer_keywords: ["IDCompositionColorMatrixEffect interface [DirectComposition]","SetMatrixElement method","IDCompositionColorMatrixEffect.SetMatrixElement","IDCompositionColorMatrixEffect.SetMatrixElement(int","int","IDCompositionAnimation)","IDCompositionColorMatrixEffect::SetMatrixElement","IDCompositionColorMatrixEffect::SetMatrixElement(int","int","IDCompositionAnimation)","SetMatrixElement","SetMatrixElement method [DirectComposition]","SetMatrixElement method [DirectComposition]","IDCompositionColorMatrixEffect interface","dcomp/IDCompositionColorMatrixEffect::SetMatrixElement","directcomp.idcompositioncolormatrixeffect_setmatrixelement_2"]
old-location: directcomp\idcompositioncolormatrixeffect_setmatrixelement_2.htm
tech.root: directcomp
ms.assetid: 370B4908-0474-4AD1-8D0A-735090F438FD
ms.date: 12/05/2018
ms.keywords: IDCompositionColorMatrixEffect interface [DirectComposition],SetMatrixElement method, IDCompositionColorMatrixEffect.SetMatrixElement, IDCompositionColorMatrixEffect.SetMatrixElement(int,int,IDCompositionAnimation), IDCompositionColorMatrixEffect::SetMatrixElement, IDCompositionColorMatrixEffect::SetMatrixElement(int,int,IDCompositionAnimation), SetMatrixElement, SetMatrixElement method [DirectComposition], SetMatrixElement method [DirectComposition],IDCompositionColorMatrixEffect interface, dcomp/IDCompositionColorMatrixEffect::SetMatrixElement, directcomp.idcompositioncolormatrixeffect_setmatrixelement_2
f1_keywords:
- dcomp/IDCompositionColorMatrixEffect.SetMatrixElement
dev_langs:
- c++
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
- IDCompositionColorMatrixEffect.SetMatrixElement
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionColorMatrixEffect::SetMatrixElement(int,int,IDCompositionAnimation)


## -description


Sets an element of the color matrix.


## -parameters




### -param row [in]

Type: <b>int</b>

The row of the element.


### -param column [in]

Type: <b>int</b>

The column of the element.


### -param animation [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the element value changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositioncolormatrixeffect">IDCompositionColorMatrixEffect</a>
 

 

