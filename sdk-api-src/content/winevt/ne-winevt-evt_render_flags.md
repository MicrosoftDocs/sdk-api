---
UID: NE:winevt._EVT_RENDER_FLAGS
title: EVT_RENDER_FLAGS (winevt.h)
description: Defines the values that specify what to render.
helpviewer_keywords: ["EVT_RENDER_FLAGS","EVT_RENDER_FLAGS enumeration [EventLog]","EvtRenderBookmark","EvtRenderEventValues","EvtRenderEventXml","wes.evt_render_flags","winevt/EVT_RENDER_FLAGS","winevt/EvtRenderBookmark","winevt/EvtRenderEventValues","winevt/EvtRenderEventXml"]
old-location: wes\evt_render_flags.htm
tech.root: wes
ms.assetid: e7206481-c734-425f-a2b6-fa0d9a2b66c1
ms.date: 12/05/2018
ms.keywords: EVT_RENDER_FLAGS, EVT_RENDER_FLAGS enumeration [EventLog], EvtRenderBookmark, EvtRenderEventValues, EvtRenderEventXml, wes.evt_render_flags, winevt/EVT_RENDER_FLAGS, winevt/EvtRenderBookmark, winevt/EvtRenderEventValues, winevt/EvtRenderEventXml
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
req.typenames: EVT_RENDER_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_RENDER_FLAGS
 - winevt/_EVT_RENDER_FLAGS
 - EVT_RENDER_FLAGS
 - winevt/EVT_RENDER_FLAGS
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
 - EVT_RENDER_FLAGS
---

# EVT_RENDER_FLAGS enumeration


## -description

Defines the values that specify what to render.

## -enum-fields

### -field EvtRenderEventValues:0

Render the event properties specified in the rendering context.

### -field EvtRenderEventXml

Render the event as an XML string. For details on the contents of the XML string, see the <a href="/windows/desktop/WES/eventschema-schema">Event</a> schema.

### -field EvtRenderBookmark

Render the bookmark as an XML string, so that you can easily persist the bookmark for use later.
