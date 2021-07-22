---
UID: NF:dcomp.IDCompositionVisual3.SetOpacity(IDCompositionAnimation)
title: IDCompositionVisual3::SetOpacity(IDCompositionAnimation) (dcomp.h)
description: Animates the value of the visual's opacity property.
helpviewer_keywords: ["IDCompositionVisual3 interface [DirectComposition]","SetOpacity method","IDCompositionVisual3.SetOpacity","IDCompositionVisual3.SetOpacity(IDCompositionAnimation)","IDCompositionVisual3::SetOpacity","IDCompositionVisual3::SetOpacity(IDCompositionAnimation)","IDCompositionVisual3::SetOpacity(IDCompositionAnimation*)","SetOpacity","SetOpacity method [DirectComposition]","SetOpacity method [DirectComposition]","IDCompositionVisual3 interface","dcomp/IDCompositionVisual3::SetOpacity","directcomp.idcompositionvisual3_setopacity_2"]
old-location: directcomp\idcompositionvisual3_setopacity_2.htm
tech.root: directcomp
ms.assetid: 84A9E6FD-8C30-4BBE-BEDD-D4C24BC6752C
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual3 interface [DirectComposition],SetOpacity method, IDCompositionVisual3.SetOpacity, IDCompositionVisual3.SetOpacity(IDCompositionAnimation), IDCompositionVisual3::SetOpacity, IDCompositionVisual3::SetOpacity(IDCompositionAnimation), IDCompositionVisual3::SetOpacity(IDCompositionAnimation*), SetOpacity, SetOpacity method [DirectComposition], SetOpacity method [DirectComposition],IDCompositionVisual3 interface, dcomp/IDCompositionVisual3::SetOpacity, directcomp.idcompositionvisual3_setopacity_2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionVisual3::SetOpacity
 - dcomp/IDCompositionVisual3::SetOpacity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionVisual3.SetOpacity
---

# IDCompositionVisual3::SetOpacity(IDCompositionAnimation)


## -description

Animates the value of the visual's opacity property.

## -parameters

### -param animation [in]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

The animation that will be used to control the value of the opacity property.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual3">IDCompositionVisual3</a>