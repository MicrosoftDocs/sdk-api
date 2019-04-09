---
UID: NF:interactioncontext.GetInteractionConfigurationInteractionContext
title: GetInteractionConfigurationInteractionContext function (interactioncontext.h)
author: windows-sdk-content
description: Gets interaction configuration state for the Interaction Context object.
old-location: input_intcontext\getinteractionconfigurationinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: 30996835-420a-4141-838f-10b62b562992
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetInteractionConfigurationInteractionContext, GetInteractionConfigurationInteractionContext function, input_intcontext.getinteractionconfigurationinteractioncontext, interactioncontext.getinteractionconfigurationinteractioncontext, interactioncontext/GetInteractionConfigurationInteractionContext
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
 - API-MS-Win-Input-IE-InteractionContext-l1-1-0.dll
 - IE_Shims.dll
api_name:
 - GetInteractionConfigurationInteractionContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetInteractionConfigurationInteractionContext function


## -description


Gets interaction configuration state  for the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


## -parameters




### -param interactionContext [in]

Pointer to a handle for the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a>.


### -param configurationCount [in]

Number of interaction configurations.


### -param configuration [out]

The interactions enabled for this <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0cbae801-d6d9-412b-ab8a-0b6c9d7c103e">INTERACTION_CONTEXT_CONFIGURATION</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>



<a href="https://msdn.microsoft.com/e792e7bc-1c7f-4fa1-810d-97391cbcf797">SetInteractionConfigurationInteractionContext</a>
 

 

