---
UID: NF:interactioncontext.GetCrossSlideParameterInteractionContext
title: GetCrossSlideParameterInteractionContext function
author: windows-sdk-content
description: Gets the cross-slide interaction behavior.
old-location: input_intcontext\getcrossslideparameterinteractioncontext.htm
old-project: Input_IntContext
ms.assetid: 19e934c6-8cd7-4302-a903-bd7865aef908
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: GetCrossSlideParameterInteractionContext, GetCrossSlideParameterInteractionContext function, input_intcontext.getcrossslideparameterinteractioncontext, interactioncontext.getcrossslideparameterinteractioncontext, interactioncontext/GetCrossSlideParameterInteractionContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MOUSE_WHEEL_PARAMETER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ninput.dll
api_name:
 - GetCrossSlideParameterInteractionContext
product: Windows
targetos: Windows
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetCrossSlideParameterInteractionContext function


## -description


Gets the cross-slide interaction behavior. 


## -parameters




### -param interactionContext [in]

The handle of the interaction context.


### -param threshold [in]

One of the constants from <a href="https://msdn.microsoft.com/c498e2ae-a761-4f93-9ec2-4030b03e64b9">CROSS_SLIDE_THRESHOLD</a>.


### -param distance [out]

The distance threshold of <i>threshold</i>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/3871f24e-34a4-4524-801d-4d60cf6165d9">CROSS_SLIDE_PARAMETER</a>



<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>



<a href="https://msdn.microsoft.com/b4d9459a-7b07-4316-bf5c-628de08de7dc">SetCrossSlideParametersInteractionContext</a>
 

 

