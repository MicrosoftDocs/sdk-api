---
UID: NE:peninputpanel.__MIDL___MIDL_itf_peninputpanel_0000_0000_0002
title: "__MIDL___MIDL_itf_peninputpanel_0000_0000_0002"
author: windows-sdk-content
description: Specifies the In-Place state values of the Tablet PC Input Panel.
old-location: tablet\inplacestate.htm
tech.root: tablet
ms.assetid: 95642cbf-4520-44cc-95ba-80de1fe3b447
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: 95642cbf-4520-44cc-95ba-80de1fe3b447, InPlaceState, InPlaceState enumeration [Tablet PC], InPlaceState_Auto, InPlaceState_Expanded, InPlaceState_HoverTarget, __MIDL___MIDL_itf_peninputpanel_0000_0000_0002, peninputpanel/InPlaceState, peninputpanel/InPlaceState_Auto, peninputpanel/InPlaceState_Expanded, peninputpanel/InPlaceState_HoverTarget, tablet.inplacestate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peninputpanel.h
api_name:
 - InPlaceState
product: Windows
targetos: Windows
req.typenames: InPlaceState
req.redist: 
---

# __MIDL___MIDL_itf_peninputpanel_0000_0000_0002 enumeration


## -description



Specifies the In-Place state values of the Tablet PC Input Panel.




## -enum-fields




### -field InPlaceState_Auto

The system decides which In-Place state of the Input Panel is the most appropriate.


### -field InPlaceState_HoverTarget

 The Input Panel Icon appears. The expanded Input Panel will not appear.


### -field InPlaceState_Expanded

The In-Place Input Panel always appears expanded, rather than the Input Panel Icon appearing first and then requiring the user to tap the Input Panel Icon before Input Panel expands.


## -remarks



The system default is for the In-Place Input Panel to appear in the hover state unless Input Panel is already visible in the expanded state, in which case Input Panel remains expanded.



