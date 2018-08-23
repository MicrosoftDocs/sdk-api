---
UID: NF:dcomp.IDCompositionEffectGroup.SetOpacity(float)
title: IDCompositionEffectGroup::SetOpacity(float)
author: windows-sdk-content
description: Changes the value of the Opacity property.
old-location: directcomp\idcompositioneffectgroup_setopacity_double.htm
old-project: directcomp
ms.assetid: B82E6BEB-CF92-4EA6-8157-5AA0A41282F1
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionEffectGroup interface [DirectComposition],SetOpacity method, IDCompositionEffectGroup.SetOpacity, IDCompositionEffectGroup.SetOpacity(float), IDCompositionEffectGroup::SetOpacity, IDCompositionEffectGroup::SetOpacity(float), SetOpacity, SetOpacity method [DirectComposition], SetOpacity method [DirectComposition],IDCompositionEffectGroup interface, dcomp/IDCompositionEffectGroup::SetOpacity, directcomp.idcompositioneffectgroup_setopacity_double
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D2D_VECTOR_4F
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
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# IDCompositionEffectGroup::SetOpacity(float)


## -description


Changes the value of the Opacity property.


## -parameters




### -param opacity [in]

Type: <b>float</b>

The new value of the Opacity property.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



The opacity is interpreted as completely transparent for all values less than or equal to 0, and as completely opaque for all values greater than or equal to 1. All values between 0 and 1 represent partial opacity.



This method fails if the <i>opacity</i> parameter is NaN, positive infinity, or negative infinity.



If the Opacity property was previously animated, this method removes the animation and sets the Opacity property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/B8C5A4D8-F161-4383-B117-B89E85C65B19">IDCompositionEffectGroup</a>
 

 

