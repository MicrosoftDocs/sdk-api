---
UID: NF:directmanipulation.IDirectManipulationInteractionEventHandler.OnInteraction
title: IDirectManipulationInteractionEventHandler::OnInteraction
author: windows-sdk-content
description: Called when an interaction is detected.
old-location: directmanipulation\idirectmanipulationinteractioneventhandler_oninteraction.htm
old-project: directmanipulation
ms.assetid: 75822986-5691-4E2B-B6DB-A91D98B39BE8
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDirectManipulationInteractionEventHandler interface [Direct Manipulation],OnInteraction method, IDirectManipulationInteractionEventHandler.OnInteraction, IDirectManipulationInteractionEventHandler::OnInteraction, OnInteraction, OnInteraction method [Direct Manipulation], OnInteraction method [Direct Manipulation],IDirectManipulationInteractionEventHandler interface, directmanipulation.idirectmanipulationinteractioneventhandler_oninteraction, directmanipulation/IDirectManipulationInteractionEventHandler::OnInteraction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DirectManipulation.h
api_name:
-	IDirectManipulationInteractionEventHandler.OnInteraction
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationInteractionEventHandler::OnInteraction


## -description


Called when an interaction is detected.


## -parameters




### -param viewport [in]

The viewport on which the interaction was detected.


### -param interaction [in]

One of the values from <a href="https://msdn.microsoft.com/5C1C79C2-3407-4FF3-986F-D9BF51983A46">DIRECTMANIPULATION_INTERACTION_TYPE</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9B832530-54B8-4D18-A5E4-4F4CAE65073A">IDirectManipulationInteractionEventHandler</a>
 

 

