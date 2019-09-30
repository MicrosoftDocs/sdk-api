---
UID: NE:winevt._EVT_RENDER_FLAGS
title: EVT_RENDER_FLAGS (winevt.h)
author: windows-sdk-content
description: Defines the values that specify what to render.
old-location: wes\evt_render_flags.htm
tech.root: wes
ms.assetid: e7206481-c734-425f-a2b6-fa0d9a2b66c1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EVT_RENDER_FLAGS, EVT_RENDER_FLAGS enumeration [EventLog], EvtRenderBookmark, EvtRenderEventValues, EvtRenderEventXml, wes.evt_render_flags, winevt/EVT_RENDER_FLAGS, winevt/EvtRenderBookmark, winevt/EvtRenderEventValues, winevt/EvtRenderEventXml
ms.topic: enum
f1_keywords: 
 - "winevt/EVT_RENDER_FLAGS"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_RENDER_FLAGS
targetos: Windows
req.typenames: EVT_RENDER_FLAGS
req.redist: 
ms.custom: 19H1
---

# EVT_RENDER_FLAGS enumeration


## -description


Defines the values that specify what to render.


## -enum-fields




### -field EvtRenderEventValues

Render the event properties specified in the rendering context.


### -field EvtRenderEventXml

Render the event as an XML string. For details on the contents of the XML string, see the <a href="https://docs.microsoft.com/windows/desktop/WES/eventschema-schema">Event</a> schema.


### -field EvtRenderBookmark

Render the bookmark as an XML string, so that you can easily persist the bookmark for use later.

