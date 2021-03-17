---
UID: NF:interactioncontext.SetInertiaParameterInteractionContext
title: SetInertiaParameterInteractionContext function (interactioncontext.h)
description: Configures the inertia behavior of a manipulation (translation, rotation, scaling) after the contact is lifted.
helpviewer_keywords: ["SetInertiaParameterInteractionContext","SetInertiaParameterInteractionContext function","input_intcontext.setinertiaparameterinteractioncontext","interactioncontext.setinertiaparameterinteractioncontext","interactioncontext/SetInertiaParameterInteractionContext"]
old-location: input_intcontext\setinertiaparameterinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: 5b228339-3830-407f-a8ea-55f40156cc32
ms.date: 12/05/2018
ms.keywords: SetInertiaParameterInteractionContext, SetInertiaParameterInteractionContext function, input_intcontext.setinertiaparameterinteractioncontext, interactioncontext.setinertiaparameterinteractioncontext, interactioncontext/SetInertiaParameterInteractionContext
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
 - SetInertiaParameterInteractionContext
 - interactioncontext/SetInertiaParameterInteractionContext
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
 - SetInertiaParameterInteractionContext
---

# SetInertiaParameterInteractionContext function


## -description

Configures the inertia behavior of a manipulation (translation, rotation, scaling) after the contact is lifted.

## -parameters

### -param interactionContext [in]

The handle of the interaction context.

### -param inertiaParameter [in]

One of the constants from <a href="/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-inertia_parameter">INERTIA_PARAMETER</a>.

### -param value [in]

One of the following:

<ul>
<li>The rate of deceleration, in radians/ms².</li>
<li>For translation, the relative change in screen location, in HIMETRIC units.</li>
<li>For rotation, the relative change in angle of rotation, in radianx</li>
<li>For scaling, the relative change in size, in HIMETRIC units.</li>
</ul>

## -returns

If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.

## -remarks

<a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> uses the inertia system setting for all manipulations (translation, rotation, scaling). This function overrides the system setting.

To restore the system setting, set <i>value</i> to INERTIA_PARAMETER_INVALID_VALUE    FLT_MAX.

## -see-also

<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-getinertiaparameterinteractioncontext">GetInertiaParameterInteractionContext</a>



<a href="/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>