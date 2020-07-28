---
UID: NE:peninputpanel.__MIDL___MIDL_itf_peninputpanel_0000_0000_0007
title: EventMask (peninputpanel.h)
description: The events on the ITextInputPanel Interface that you can set attention for.
helpviewer_keywords: ["83fefdcf-eb5f-4fb6-b107-dc8abce02bb6","EventMask","EventMask enumeration [Tablet PC]","EventMask_All","EventMask_CorrectionModeChanged","EventMask_CorrectionModeChanging","EventMask_InPlaceSizeChanged","EventMask_InPlaceSizeChanging","EventMask_InPlaceStateChanged","EventMask_InPlaceStateChanging","EventMask_InPlaceVisibilityChanged","EventMask_InPlaceVisibilityChanging","EventMask_InputAreaChanged","EventMask_InputAreaChanging","EventMask_TextInserted","EventMask_TextInserting","peninputpanel/EventMask","peninputpanel/EventMask_All","peninputpanel/EventMask_CorrectionModeChanged","peninputpanel/EventMask_CorrectionModeChanging","peninputpanel/EventMask_InPlaceSizeChanged","peninputpanel/EventMask_InPlaceSizeChanging","peninputpanel/EventMask_InPlaceStateChanged","peninputpanel/EventMask_InPlaceStateChanging","peninputpanel/EventMask_InPlaceVisibilityChanged","peninputpanel/EventMask_InPlaceVisibilityChanging","peninputpanel/EventMask_InputAreaChanged","peninputpanel/EventMask_InputAreaChanging","peninputpanel/EventMask_TextInserted","peninputpanel/EventMask_TextInserting","tablet.eventmask"]
old-location: tablet\eventmask.htm
tech.root: tablet
ms.assetid: 83fefdcf-eb5f-4fb6-b107-dc8abce02bb6
ms.date: 12/05/2018
ms.keywords: 83fefdcf-eb5f-4fb6-b107-dc8abce02bb6, EventMask, EventMask enumeration [Tablet PC], EventMask_All, EventMask_CorrectionModeChanged, EventMask_CorrectionModeChanging, EventMask_InPlaceSizeChanged, EventMask_InPlaceSizeChanging, EventMask_InPlaceStateChanged, EventMask_InPlaceStateChanging, EventMask_InPlaceVisibilityChanged, EventMask_InPlaceVisibilityChanging, EventMask_InputAreaChanged, EventMask_InputAreaChanging, EventMask_TextInserted, EventMask_TextInserting, peninputpanel/EventMask, peninputpanel/EventMask_All, peninputpanel/EventMask_CorrectionModeChanged, peninputpanel/EventMask_CorrectionModeChanging, peninputpanel/EventMask_InPlaceSizeChanged, peninputpanel/EventMask_InPlaceSizeChanging, peninputpanel/EventMask_InPlaceStateChanged, peninputpanel/EventMask_InPlaceStateChanging, peninputpanel/EventMask_InPlaceVisibilityChanged, peninputpanel/EventMask_InPlaceVisibilityChanging, peninputpanel/EventMask_InputAreaChanged, peninputpanel/EventMask_InputAreaChanging, peninputpanel/EventMask_TextInserted, peninputpanel/EventMask_TextInserting, tablet.eventmask
f1_keywords:
- peninputpanel/EventMask
dev_langs:
- c++
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
- EventMask
targetos: Windows
req.typenames: EventMask
req.redist: 
ms.custom: 19H1
---

# EventMask enumeration


## -description



The events on the <a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a> that you can set attention for.




## -enum-fields




### -field EventMask_InPlaceStateChanging

Occurs when the correction mode is about to change.
          


### -field EventMask_InPlaceStateChanged

Occurs when the correction mode has changed.
          


### -field EventMask_InPlaceSizeChanging

Occurs when the in-place Input Panel size is about to change due to user resizing, auto growth or an input area change.
          


### -field EventMask_InPlaceSizeChanged

Occurs when the in-place Input Panel size has changed due to a user resize, auto growth, or an input area change.
          


### -field EventMask_InputAreaChanging

Occurs when the input area is about to change.
          


### -field EventMask_InputAreaChanged

Occurs when the input area has changed.
          


### -field EventMask_CorrectionModeChanging

Occurs when the correction mode is about to change.
          


### -field EventMask_CorrectionModeChanged

Occurs when the correction mode has changed.
          


### -field EventMask_InPlaceVisibilityChanging

Occurs when the in-place Input Panel visibility is about to change.
          


### -field EventMask_InPlaceVisibilityChanged

Occurs when the input area has changed.
          


### -field EventMask_TextInserting

Occurs when Tablet PC Input Panel is about to insert text into the control with input focus.
          


### -field EventMask_TextInserted

Occurs when the Tablet PC Input Panel has inserted text into the control with input focus.
          


### -field EventMask_All

Represents a bitwise combination of all member events.
          


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-advise">ITextInputPanel::Advise Method</a>
 

 

