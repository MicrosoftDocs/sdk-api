---
UID: NF:interactioncontext.GetCrossSlideParameterInteractionContext
title: GetCrossSlideParameterInteractionContext function (interactioncontext.h)
author: windows-sdk-content
description: Gets the cross-slide interaction behavior.
old-location: input_intcontext\getcrossslideparameterinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: 19e934c6-8cd7-4302-a903-bd7865aef908
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCrossSlideParameterInteractionContext, GetCrossSlideParameterInteractionContext function, input_intcontext.getcrossslideparameterinteractioncontext, interactioncontext.getcrossslideparameterinteractioncontext, interactioncontext/GetCrossSlideParameterInteractionContext
ms.topic: function
f1_keywords: 
 - "interactioncontext/GetCrossSlideParameterInteractionContext"
req.header: interactioncontext.h
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
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ninput.dll
api_name:
 - GetCrossSlideParameterInteractionContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCrossSlideParameterInteractionContext function


## -description


Gets the cross-slide interaction behavior. 


## -parameters




### -param interactionContext [in]

The handle of the interaction context.


### -param threshold [in]

One of the constants from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-cross_slide_threshold">CROSS_SLIDE_THRESHOLD</a>.


### -param distance [out]

The distance threshold of <i>threshold</i>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-cross_slide_parameter">CROSS_SLIDE_PARAMETER</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setcrossslideparametersinteractioncontext">SetCrossSlideParametersInteractionContext</a>
 

 

