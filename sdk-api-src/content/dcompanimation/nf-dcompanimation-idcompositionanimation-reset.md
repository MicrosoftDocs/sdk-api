---
UID: NF:dcompanimation.IDCompositionAnimation.Reset
title: IDCompositionAnimation::Reset
author: windows-sdk-content
description: Resets the animation function so that it contains no segments.
old-location: directcomp\idcompositionanimation_reset.htm
old-project: directcomp
ms.assetid: 3745fff0-eefa-4262-9ce3-9ab812264c1d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDCompositionAnimation interface [DirectComposition],Reset method, IDCompositionAnimation.Reset, IDCompositionAnimation::Reset, Reset, Reset method [DirectComposition], Reset method [DirectComposition],IDCompositionAnimation interface, dcompanimation/IDCompositionAnimation::Reset, directcomp.idcompositionanimation_reset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dcompanimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DcompAnimation.idl
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
 - IDCompositionAnimation.Reset
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# IDCompositionAnimation::Reset


## -description


Resets the animation function so that it contains no segments.


## -parameters






## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method returns the animation function to a clean state, as when the animation was first constructed. After this method is called, the next segment to be added becomes the first segment of the animation function. Because it is the first segment, it can have any non-negative beginning offset.




## -see-also




<a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>
 

 

