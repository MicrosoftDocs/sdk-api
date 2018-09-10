---
UID: NF:interactioncontext.SetInteractionConfigurationInteractionContext
title: SetInteractionConfigurationInteractionContext function
author: windows-sdk-content
description: Configures the Interaction Context object to process the specified manipulations.
old-location: input_intcontext\setinteractionconfigurationinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: e792e7bc-1c7f-4fa1-810d-97391cbcf797
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: SetInteractionConfigurationInteractionContext, SetInteractionConfigurationInteractionContext function, input_intcontext.setinteractionconfigurationinteractioncontext, interactioncontext.setinteractionconfigurationinteractioncontext, interactioncontext/SetInteractionConfigurationInteractionContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: interactioncontext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Ninput.dll; Edgehtml.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ninput.dll
 - edgehtml.dll
 - API-MS-Win-Input-IE-InteractionContext-l1-1-0.dll
 - IE_Shims.dll
api_name:
 - SetInteractionConfigurationInteractionContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetInteractionConfigurationInteractionContext function


## -description


Configures the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object to process the specified manipulations.


## -parameters




### -param interactionContext [in]

The handle of the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a>.


### -param configurationCount [in]

The number of interactions being configured. 


### -param configuration [in]

The interactions to enable for this <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



By default, no configuration flags are set (no interactions are enabled). Each interaction must be explicitly declared.

Configuration changes are applied only to new interactions.




## -see-also




<a href="https://msdn.microsoft.com/30996835-420a-4141-838f-10b62b562992">GetInteractionConfigurationInteractionContext</a>



<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0cbae801-d6d9-412b-ab8a-0b6c9d7c103e">INTERACTION_CONTEXT_CONFIGURATION</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>
 

 

