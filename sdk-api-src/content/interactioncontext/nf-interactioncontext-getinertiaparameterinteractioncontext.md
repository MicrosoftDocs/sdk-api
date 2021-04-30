---
UID: NF:interactioncontext.GetInertiaParameterInteractionContext
title: GetInertiaParameterInteractionContext function (interactioncontext.h)
description: Gets the inertia behavior of a manipulation (translation, rotation, scaling).
helpviewer_keywords: ["GetInertiaParameterInteractionContext","GetInertiaParameterInteractionContext function","input_intcontext.getinertiaparameterinteractioncontext","interactioncontext.getinertiaparameterinteractioncontext","interactioncontext/GetInertiaParameterInteractionContext"]
old-location: input_intcontext\getinertiaparameterinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: e3ae71e2-be61-49c1-82a1-2fa82fe9a7ba
ms.date: 12/05/2018
ms.keywords: GetInertiaParameterInteractionContext, GetInertiaParameterInteractionContext function, input_intcontext.getinertiaparameterinteractioncontext, interactioncontext.getinertiaparameterinteractioncontext, interactioncontext/GetInertiaParameterInteractionContext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetInertiaParameterInteractionContext
 - interactioncontext/GetInertiaParameterInteractionContext
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
 - GetInertiaParameterInteractionContext
---

# GetInertiaParameterInteractionContext function


## -description

Gets the inertia behavior of a manipulation (translation, rotation, scaling).

## -parameters

### -param interactionContext [in]

The handle of the interaction context.

### -param inertiaParameter [in]

One of the constants from <a href="/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-inertia_parameter">INERTIA_PARAMETER</a>.

### -param value [out]

The value of <i>inertiaParameter</i>. This value is one of the following:

<ul>
<li>The rate of deceleration, in radians/ms².</li>
<li>For translation, the relative change in screen location, in HIMETRIC units.</li>
<li>For rotation, the relative change in angle of rotation, in radians</li>
<li>For scaling, the relative change in size, in HIMETRIC units.</li>
</ul>

## -returns

If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.

## -see-also

<a href="/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setinertiaparameterinteractioncontext">SetInertiaParameterInteractionContext</a>