---
UID: NF:dcomp.IDCompositionEffectGroup.SetOpacity(IDCompositionAnimation)
title: IDCompositionEffectGroup::SetOpacity(IDCompositionAnimation) (dcomp.h)
author: windows-sdk-content
description: Animates the value of the Opacity property.
old-location: directcomp\idcompositioneffectgroup_setopacity_idcompositionanimation.htm
tech.root: directcomp
ms.assetid: 9BD576D6-51CA-41A5-AF8F-FEA77C17C872
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionEffectGroup interface [DirectComposition],SetOpacity method, IDCompositionEffectGroup.SetOpacity, IDCompositionEffectGroup.SetOpacity(IDCompositionAnimation), IDCompositionEffectGroup::SetOpacity, IDCompositionEffectGroup::SetOpacity(IDCompositionAnimation), IDCompositionEffectGroup::SetOpacity(IDCompositionAnimation*), SetOpacity, SetOpacity method [DirectComposition], SetOpacity method [DirectComposition],IDCompositionEffectGroup interface, dcomp/IDCompositionEffectGroup::SetOpacity, directcomp.idcompositioneffectgroup_setopacity_idcompositionanimation
ms.topic: method
f1_keywords: ["dcomp/IDCompositionEffectGroup.SetOpacity"]
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
 - IDCompositionEffectGroup.SetOpacity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionEffectGroup::SetOpacity(IDCompositionAnimation)


## -description


Animates the value of the Opacity property. 


## -parameters




### -param animation [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>*</b>

An animation that represents how the value of the Opacity property changes over time. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method makes a copy of the specified animation. If the object referenced by the <i>animation</i> parameter is changed after calling this method, the change does not affect the Opacity property unless this method is called again. If the Opacity property was previously animated, calling this method replaces the previous animation with the new animation. 



This method fails if <i>animation</i> is an invalid pointer or if it was not created by the same <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as the affected compostion effect group. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffectgroup">IDCompositionEffectGroup</a>
 

 

