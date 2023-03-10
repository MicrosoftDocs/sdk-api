---
UID: NE:peninputpanel.__MIDL___MIDL_itf_peninputpanel_0000_0000_0002
title: InPlaceState (peninputpanel.h)
description: Specifies the In-Place state values of the Tablet PC Input Panel.
helpviewer_keywords: ["95642cbf-4520-44cc-95ba-80de1fe3b447","InPlaceState","InPlaceState enumeration [Tablet PC]","InPlaceState_Auto","InPlaceState_Expanded","InPlaceState_HoverTarget","peninputpanel/InPlaceState","peninputpanel/InPlaceState_Auto","peninputpanel/InPlaceState_Expanded","peninputpanel/InPlaceState_HoverTarget","tablet.inplacestate"]
old-location: tablet\inplacestate.htm
tech.root: tablet
ms.assetid: 95642cbf-4520-44cc-95ba-80de1fe3b447
ms.date: 12/05/2018
ms.keywords: 95642cbf-4520-44cc-95ba-80de1fe3b447, InPlaceState, InPlaceState enumeration [Tablet PC], InPlaceState_Auto, InPlaceState_Expanded, InPlaceState_HoverTarget, peninputpanel/InPlaceState, peninputpanel/InPlaceState_Auto, peninputpanel/InPlaceState_Expanded, peninputpanel/InPlaceState_HoverTarget, tablet.inplacestate
req.header: peninputpanel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: InPlaceState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_peninputpanel_0000_0000_0002
 - peninputpanel/__MIDL___MIDL_itf_peninputpanel_0000_0000_0002
 - InPlaceState
 - peninputpanel/InPlaceState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peninputpanel.h
api_name:
 - InPlaceState
---

# InPlaceState enumeration


## -description

Specifies the In-Place state values of the Tablet PC Input Panel.

## -enum-fields

### -field InPlaceState_Auto:0

The system decides which In-Place state of the Input Panel is the most appropriate.

### -field InPlaceState_HoverTarget:1

 The Input Panel Icon appears. The expanded Input Panel will not appear.

### -field InPlaceState_Expanded:2

The In-Place Input Panel always appears expanded, rather than the Input Panel Icon appearing first and then requiring the user to tap the Input Panel Icon before Input Panel expands.

## -remarks

The system default is for the In-Place Input Panel to appear in the hover state unless Input Panel is already visible in the expanded state, in which case Input Panel remains expanded.

