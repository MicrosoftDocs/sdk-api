---
UID: NE:winevt._EVT_RENDER_FLAGS
title: "_EVT_RENDER_FLAGS"
author: windows-sdk-content
description: Defines the values that specify what to render.
old-location: wes\evt_render_flags.htm
tech.root: WES
ms.assetid: e7206481-c734-425f-a2b6-fa0d9a2b66c1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EVT_RENDER_FLAGS, EVT_RENDER_FLAGS enumeration [EventLog], EvtRenderBookmark, EvtRenderEventValues, EvtRenderEventXml, _EVT_RENDER_FLAGS, wes.evt_render_flags, winevt/EVT_RENDER_FLAGS, winevt/EvtRenderBookmark, winevt/EvtRenderEventValues, winevt/EvtRenderEventXml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: EVT_RENDER_FLAGS
req.redist: 
---

# _EVT_RENDER_FLAGS enumeration


## -description


Defines the values that specify what to render.


## -enum-fields




### -field EvtRenderEventValues

Render the event properties specified in the rendering context.


### -field EvtRenderEventXml

Render the event as an XML string. For details on the contents of the XML string, see the <a href="https://msdn.microsoft.com/36037697-b777-4e5c-99af-77964200a3e4">Event</a> schema.


### -field EvtRenderBookmark

Render the bookmark as an XML string, so that you can easily persist the bookmark for use later.

