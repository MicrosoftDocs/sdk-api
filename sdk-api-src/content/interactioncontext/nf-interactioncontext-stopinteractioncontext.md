---
UID: NF:interactioncontext.StopInteractionContext
title: StopInteractionContext function (interactioncontext.h)
description: Sets the interaction state to INTERACTION_STATE_IDLE and leaves all interaction configuration settings and parameters intact.
helpviewer_keywords: ["StopInteractionContext","StopInteractionContext function","input_intcontext.stopinteractioncontext","interactioncontext.stopinteractioncontext","interactioncontext/StopInteractionContext"]
old-location: input_intcontext\stopinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: 52fb6054-c8f3-4dbe-af1f-0b8d39ebcf5b
ms.date: 12/05/2018
ms.keywords: StopInteractionContext, StopInteractionContext function, input_intcontext.stopinteractioncontext, interactioncontext.stopinteractioncontext, interactioncontext/StopInteractionContext
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
req.dll: Ninput.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StopInteractionContext
 - interactioncontext/StopInteractionContext
dev_langs:
 - c++
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
 - StopInteractionContext
---

# StopInteractionContext function

## -description

Sets the [interaction state](ne-interactioncontext-interaction_state.md) to INTERACTION_STATE_IDLE and leaves all interaction configuration settings and parameters intact. Current interactions are cancelled and notifications sent as required.
[Interaction Context](../_input_intcontext/index.md) does not have to be reconfigured before next use.

## -parameters

### -param interactionContext [in]

Handle to the [Interaction Context](../_input_intcontext/index.md) object.

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -see-also

[CreateInteractionContext function](nf-interactioncontext-createinteractioncontext.md)

[DestroyInteractionContext function](nf-interactioncontext-destroyinteractioncontext.md)

[ResetInteractionContext function](nf-interactioncontext-resetinteractioncontext.md)
