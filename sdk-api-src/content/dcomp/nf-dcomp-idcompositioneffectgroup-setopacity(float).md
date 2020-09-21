---
UID: NF:dcomp.IDCompositionEffectGroup.SetOpacity(float)
title: IDCompositionEffectGroup::SetOpacity(float) (dcomp.h)
description: Changes the value of the Opacity property.
helpviewer_keywords: ["IDCompositionEffectGroup interface [DirectComposition]","SetOpacity method","IDCompositionEffectGroup.SetOpacity","IDCompositionEffectGroup.SetOpacity(float)","IDCompositionEffectGroup::SetOpacity","IDCompositionEffectGroup::SetOpacity(float)","SetOpacity","SetOpacity method [DirectComposition]","SetOpacity method [DirectComposition]","IDCompositionEffectGroup interface","dcomp/IDCompositionEffectGroup::SetOpacity","directcomp.idcompositioneffectgroup_setopacity_double"]
old-location: directcomp\idcompositioneffectgroup_setopacity_double.htm
tech.root: directcomp
ms.assetid: B82E6BEB-CF92-4EA6-8157-5AA0A41282F1
ms.date: 12/05/2018
ms.keywords: IDCompositionEffectGroup interface [DirectComposition],SetOpacity method, IDCompositionEffectGroup.SetOpacity, IDCompositionEffectGroup.SetOpacity(float), IDCompositionEffectGroup::SetOpacity, IDCompositionEffectGroup::SetOpacity(float), SetOpacity, SetOpacity method [DirectComposition], SetOpacity method [DirectComposition],IDCompositionEffectGroup interface, dcomp/IDCompositionEffectGroup::SetOpacity, directcomp.idcompositioneffectgroup_setopacity_double
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionEffectGroup::SetOpacity
 - dcomp/IDCompositionEffectGroup::SetOpacity
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
 - IDCompositionEffectGroup.SetOpacity
---

# IDCompositionEffectGroup::SetOpacity(float)


## -description

Changes the value of the Opacity property.

## -parameters

### -param opacity [in]

Type: <b>float</b>

The new value of the Opacity property.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

The opacity is interpreted as completely transparent for all values less than or equal to 0, and as completely opaque for all values greater than or equal to 1. All values between 0 and 1 represent partial opacity.



This method fails if the <i>opacity</i> parameter is NaN, positive infinity, or negative infinity.



If the Opacity property was previously animated, this method removes the animation and sets the Opacity property to the specified static value.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffectgroup">IDCompositionEffectGroup</a>