---
UID: NE:winevt._EVT_RENDER_CONTEXT_FLAGS
title: EVT_RENDER_CONTEXT_FLAGS (winevt.h)
description: Defines the values that specify the type of information to access from the event.
helpviewer_keywords: ["EVT_RENDER_CONTEXT_FLAGS","EVT_RENDER_CONTEXT_FLAGS enumeration [EventLog]","EvtRenderContextSystem","EvtRenderContextUser","EvtRenderContextValues","wes.evt_render_context_flags","winevt/EVT_RENDER_CONTEXT_FLAGS","winevt/EvtRenderContextSystem","winevt/EvtRenderContextUser","winevt/EvtRenderContextValues"]
old-location: wes\evt_render_context_flags.htm
tech.root: wes
ms.assetid: 1c933266-28d9-4ef2-b156-eedf4ccb189b
ms.date: 12/05/2018
ms.keywords: EVT_RENDER_CONTEXT_FLAGS, EVT_RENDER_CONTEXT_FLAGS enumeration [EventLog], EvtRenderContextSystem, EvtRenderContextUser, EvtRenderContextValues, wes.evt_render_context_flags, winevt/EVT_RENDER_CONTEXT_FLAGS, winevt/EvtRenderContextSystem, winevt/EvtRenderContextUser, winevt/EvtRenderContextValues
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: EVT_RENDER_CONTEXT_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_RENDER_CONTEXT_FLAGS
 - winevt/_EVT_RENDER_CONTEXT_FLAGS
 - EVT_RENDER_CONTEXT_FLAGS
 - winevt/EVT_RENDER_CONTEXT_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_RENDER_CONTEXT_FLAGS
---

# EVT_RENDER_CONTEXT_FLAGS enumeration


## -description

Defines the values that specify the type of information to access from the event. These flags cannot be combined.

## -enum-fields

### -field EvtRenderContextValues:0

Render specific properties from the event.

### -field EvtRenderContextSystem

Render the system properties under the **System** element. The properties are returned in the order defined in the [EVT_SYSTEM_PROPERTY_ID enumeration](ne-winevt-evt_system_property_id.md).

### -field EvtRenderContextUser

Render all user-defined properties under the **UserData** or **EventData** element. If the data template associated with the event contains a **UserData** section, the **UserData** properties are rendered; otherwise, the **EventData** properties are rendered.

## -remarks

## -see-also

[EvtCreateRenderContext function](nf-winevt-evtcreaterendercontext.md)
