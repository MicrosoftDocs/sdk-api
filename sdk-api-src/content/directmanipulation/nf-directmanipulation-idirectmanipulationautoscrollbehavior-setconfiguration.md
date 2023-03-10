---
UID: NF:directmanipulation.IDirectManipulationAutoScrollBehavior.SetConfiguration
title: IDirectManipulationAutoScrollBehavior::SetConfiguration (directmanipulation.h)
description: Performs the auto-scroll animation for the viewport this behavior is attached to.
helpviewer_keywords: ["IDirectManipulationAutoScrollBehavior interface [Direct Manipulation]","SetConfiguration method","IDirectManipulationAutoScrollBehavior.SetConfiguration","IDirectManipulationAutoScrollBehavior::SetConfiguration","SetConfiguration","SetConfiguration method [Direct Manipulation]","SetConfiguration method [Direct Manipulation]","IDirectManipulationAutoScrollBehavior interface","directmanipulation.idirectmanipulationautoscrollbehavior_setconfiguration","directmanipulation/IDirectManipulationAutoScrollBehavior::SetConfiguration"]
old-location: directmanipulation\idirectmanipulationautoscrollbehavior_setconfiguration.htm
tech.root: directmanipulation
ms.assetid: 2DE988EA-8690-4AF2-A545-8226032D6E83
ms.date: 12/05/2018
ms.keywords: IDirectManipulationAutoScrollBehavior interface [Direct Manipulation],SetConfiguration method, IDirectManipulationAutoScrollBehavior.SetConfiguration, IDirectManipulationAutoScrollBehavior::SetConfiguration, SetConfiguration, SetConfiguration method [Direct Manipulation], SetConfiguration method [Direct Manipulation],IDirectManipulationAutoScrollBehavior interface, directmanipulation.idirectmanipulationautoscrollbehavior_setconfiguration, directmanipulation/IDirectManipulationAutoScrollBehavior::SetConfiguration
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
 - IDirectManipulationAutoScrollBehavior::SetConfiguration
 - directmanipulation/IDirectManipulationAutoScrollBehavior::SetConfiguration
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
 - IDirectManipulationAutoScrollBehavior.SetConfiguration
---

# IDirectManipulationAutoScrollBehavior::SetConfiguration


## -description

Performs the auto-scroll animation for the viewport this behavior is attached to.

## -parameters

### -param motionTypes [in]

A combination of <b>DIRECTMANIPULATION_MOTION_TRANSLATEX</b> and <b>DIRECTMANIPULATION_MOTION_TRANSLATEY</b> from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_motion_types">DIRECTMANIPULATION_MOTION_TYPES</a>. <b>DIRECTMANIPULATION_MOTION_NONE</b> cannot be specified.

### -param scrollMotion [in]

One of the values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_autoscroll_configuration">DIRECTMANIPULATION_AUTOSCROLL_CONFIGURATION</a>.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>SetConfiguration</b> takes effect immediately. If the content is not in inertia, and <b>DIRECTMANIPULATION_AUTOSCROLL_CONFIGURATION_STOP</b> is specified for <i>scrollMotion</i>, then this method returns S_FALSE. 


#### Examples


```cpp
spAutoScrollBehavior->SetConfiguration(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_AUTOSCROLL_CONFIGURATION_FORWARD));
```

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationautoscrollbehavior">IDirectManipulationAutoScrollBehavior</a>