---
UID: NF:winevt.EvtCreateRenderContext
title: EvtCreateRenderContext function (winevt.h)
description: Creates a context that specifies the information in the event that you want to render.
helpviewer_keywords: ["EvtCreateRenderContext","EvtCreateRenderContext function [EventLog]","wes.evtcreaterendercontext","winevt/EvtCreateRenderContext"]
old-location: wes\evtcreaterendercontext.htm
tech.root: wes
ms.assetid: 729cfd74-c158-463d-9247-ee2c75b259d4
ms.date: 12/05/2018
ms.keywords: EvtCreateRenderContext, EvtCreateRenderContext function [EventLog], wes.evtcreaterendercontext, winevt/EvtCreateRenderContext
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
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EvtCreateRenderContext
 - winevt/EvtCreateRenderContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-wevtapi-eventlog-l1-1-3.dll
 - Wevtapi.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-0.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-1.dll
 - Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtCreateRenderContext
---

# EvtCreateRenderContext function


## -description

Creates a context that specifies the information in the event that you want to render.

## -parameters

### -param ValuePathsCount [in]

The number of XPath expressions in the <i>ValuePaths</i> parameter.

### -param ValuePaths [in]

An array of XPath expressions that uniquely identify a node or attribute in the event that you want to render.

Set to **NULL** if the **EvtRenderContextValues** context flag is not set in the *Flags* parameter.

The expressions must not contain the **OR** or **AND** operator. 

Attribute names in the expressions must not be followed by a space. 

### -param Flags [in]

Flag that identifies the information in the event that you want to render. For example, the system information, user information, or specific values. For possible values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_render_context_flags">EVT_RENDER_CONTEXT_FLAGS</a> enumeration.

## -returns

A context handle that you use when calling the <a href="/windows/desktop/api/winevt/nf-winevt-evtrender">EvtRender</a> function to render the contents of an event; otherwise, <b>NULL</b>. If <b>NULL</b>, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

## -remarks

To render the specified information from the event, call the  <a href="/windows/desktop/api/winevt/nf-winevt-evtrender">EvtRender</a> function.

You must call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function to close the handle when done.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/rendering-events">Rendering Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtrender">EvtRender</a>
