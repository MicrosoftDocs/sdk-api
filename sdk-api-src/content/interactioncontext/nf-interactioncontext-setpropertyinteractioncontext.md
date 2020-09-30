---
UID: NF:interactioncontext.SetPropertyInteractionContext
title: SetPropertyInteractionContext function (interactioncontext.h)
description: Sets Interaction Context object properties.
helpviewer_keywords: ["SetPropertyInteractionContext","SetPropertyInteractionContext function","input_intcontext.setpropertyinteractioncontext","interactioncontext.setpropertyinteractioncontext","interactioncontext/SetPropertyInteractionContext"]
old-location: input_intcontext\setpropertyinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: da24831e-9f9f-4a9f-92bf-60e1c5338554
ms.date: 12/05/2018
ms.keywords: SetPropertyInteractionContext, SetPropertyInteractionContext function, input_intcontext.setpropertyinteractioncontext, interactioncontext.setpropertyinteractioncontext, interactioncontext/SetPropertyInteractionContext
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
 - SetPropertyInteractionContext
 - interactioncontext/SetPropertyInteractionContext
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
 - SetPropertyInteractionContext
---

# SetPropertyInteractionContext function


## -description

Sets <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object properties.

## -parameters

### -param interactionContext [in]

Handle to the <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.

### -param contextProperty [in]

One of the constants identified by <a href="/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-interaction_context_property">INTERACTION_CONTEXT_PROPERTY</a>.

### -param value [in]

The value of the constant identified by <i>contextProperty</i>.

## -returns

If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext">AddPointerInteractionContext</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext">GetPropertyInteractionContext</a>



<a href="/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>