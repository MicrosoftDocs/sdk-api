---
UID: NF:directmanipulation.IDirectManipulationInteractionEventHandler.OnInteraction
title: IDirectManipulationInteractionEventHandler::OnInteraction (directmanipulation.h)
description: Called when an interaction is detected.
helpviewer_keywords: ["IDirectManipulationInteractionEventHandler interface [Direct Manipulation]","OnInteraction method","IDirectManipulationInteractionEventHandler.OnInteraction","IDirectManipulationInteractionEventHandler::OnInteraction","OnInteraction","OnInteraction method [Direct Manipulation]","OnInteraction method [Direct Manipulation]","IDirectManipulationInteractionEventHandler interface","directmanipulation.idirectmanipulationinteractioneventhandler_oninteraction","directmanipulation/IDirectManipulationInteractionEventHandler::OnInteraction"]
old-location: directmanipulation\idirectmanipulationinteractioneventhandler_oninteraction.htm
tech.root: directmanipulation
ms.assetid: 75822986-5691-4E2B-B6DB-A91D98B39BE8
ms.date: 12/05/2018
ms.keywords: IDirectManipulationInteractionEventHandler interface [Direct Manipulation],OnInteraction method, IDirectManipulationInteractionEventHandler.OnInteraction, IDirectManipulationInteractionEventHandler::OnInteraction, OnInteraction, OnInteraction method [Direct Manipulation], OnInteraction method [Direct Manipulation],IDirectManipulationInteractionEventHandler interface, directmanipulation.idirectmanipulationinteractioneventhandler_oninteraction, directmanipulation/IDirectManipulationInteractionEventHandler::OnInteraction
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectManipulationInteractionEventHandler::OnInteraction
 - directmanipulation/IDirectManipulationInteractionEventHandler::OnInteraction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationInteractionEventHandler.OnInteraction
---

# IDirectManipulationInteractionEventHandler::OnInteraction


## -description

Called when an interaction is detected.

## -parameters

### -param viewport [in]

The viewport on which the interaction was detected.

### -param interaction [in]

One of the values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_interaction_type">DIRECTMANIPULATION_INTERACTION_TYPE</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationinteractioneventhandler">IDirectManipulationInteractionEventHandler</a>