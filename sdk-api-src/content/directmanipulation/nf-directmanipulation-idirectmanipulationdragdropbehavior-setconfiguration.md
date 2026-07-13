---
UID: NF:directmanipulation.IDirectManipulationDragDropBehavior.SetConfiguration
title: IDirectManipulationDragDropBehavior::SetConfiguration (directmanipulation.h)
description: Sets the configuration of the drag-drop interaction for the viewport this behavior is attached to.
helpviewer_keywords: ["IDirectManipulationDragDropBehavior interface [Direct Manipulation]","SetConfiguration method","IDirectManipulationDragDropBehavior.SetConfiguration","IDirectManipulationDragDropBehavior::SetConfiguration","SetConfiguration","SetConfiguration method [Direct Manipulation]","SetConfiguration method [Direct Manipulation]","IDirectManipulationDragDropBehavior interface","directmanipulation.idirectmanipulationdragdropbehavior_setconfiguration","directmanipulation/IDirectManipulationDragDropBehavior::SetConfiguration"]
old-location: directmanipulation\idirectmanipulationdragdropbehavior_setconfiguration.htm
tech.root: directmanipulation
ms.assetid: 972EF04E-B14C-4EF9-B40A-EAF0458F2947
ms.date: 12/05/2018
ms.keywords: IDirectManipulationDragDropBehavior interface [Direct Manipulation],SetConfiguration method, IDirectManipulationDragDropBehavior.SetConfiguration, IDirectManipulationDragDropBehavior::SetConfiguration, SetConfiguration, SetConfiguration method [Direct Manipulation], SetConfiguration method [Direct Manipulation],IDirectManipulationDragDropBehavior interface, directmanipulation.idirectmanipulationdragdropbehavior_setconfiguration, directmanipulation/IDirectManipulationDragDropBehavior::SetConfiguration
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
 - IDirectManipulationDragDropBehavior::SetConfiguration
 - directmanipulation/IDirectManipulationDragDropBehavior::SetConfiguration
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
 - IDirectManipulationDragDropBehavior.SetConfiguration
---

# IDirectManipulationDragDropBehavior::SetConfiguration


## -description

Sets the configuration of the drag-drop interaction for the viewport this behavior is attached to.

## -parameters

### -param configuration [in]

Combination  of values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_drag_drop_configuration">DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION</a>.

For the configuration to be valid, <i>configuration</i> must contain exactly one of the following three values:
<ul>
<li><b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_ONLY</b></li>
<li><b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_DRAG</b></li>
<li><b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HOLD_DRAG</b></li>
</ul>


If <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_ONLY</b> or  <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_SELECT_DRAG</b> is specified, one of <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_VERTICAL</b> or <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HORIZONTAL</b> is required.


If <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HOLD_DRAG</b> is specified, both <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_VERTICAL</b> and <b>DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION_HORIZONTAL</b> are required.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The configuration of the behavior can be set before or after it has been added to a viewport. If a configuration change is made while an interaction is occurring, the new configuration takes effect on the next interaction.

 



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration">IDirectManipulationViewport::ActivateConfiguration</a> should not be called prior to calling <b>IDirectManipulationDragDropBehavior::SetConfiguration</b>. This will result in  unexpected behavior.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationdragdropbehavior">IDirectManipulationDragDropBehavior</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration">IDirectManipulationViewport::ActivateConfiguration</a>