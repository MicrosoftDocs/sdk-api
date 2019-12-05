---
UID: NF:winevt.EvtCreateRenderContext
title: EvtCreateRenderContext function (winevt.h)
description: Creates a context that specifies the information in the event that you want to render.
old-location: wes\evtcreaterendercontext.htm
tech.root: wes
ms.assetid: 729cfd74-c158-463d-9247-ee2c75b259d4
ms.date: 12/05/2018
ms.keywords: EvtCreateRenderContext, EvtCreateRenderContext function [EventLog], wes.evtcreaterendercontext, winevt/EvtCreateRenderContext
ms.topic: function
f1_keywords:
- winevt/EvtCreateRenderContext
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wevtapi.dll
- Ext-MS-Win-WEvtAPI-EventLog-L1-1-0.dll
- Ext-MS-Win-WEvtAPI-EventLog-L1-1-1.dll
- Ext-MS-Win-WEvtAPI-EventLog-L1-1-2.dll
api_name:
- EvtCreateRenderContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EvtCreateRenderContext function


## -description


Creates a context that specifies the information in the event that you want to render.


## -parameters




### -param ValuePathsCount [in]

The number of XPath expressions in the <i>ValuePaths</i> parameter.


### -param ValuePaths [in]

An array of XPath expressions that uniquely identify a node or attribute in the event that you want to render. The expressions must not contain the <b>OR</b> or <b>AND</b> operator. Set to <b>NULL</b> if the <b>EvtRenderContextValues</b> context flag is not set in the <i>Flags</i> parameter.


### -param Flags [in]

One or more flags that identify the information in the event that you want to render. For example, the system information, user information, or specific values. For possible values, see the <a href="https://docs.microsoft.com/windows/desktop/api/winevt/ne-winevt-evt_render_context_flags">EVT_RENDER_CONTEXT_FLAGS</a> enumeration.


## -returns



A context handle that you use when calling the <a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtrender">EvtRender</a> function to render the contents of an event; otherwise, <b>NULL</b>. If <b>NULL</b>, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.




## -remarks



To render the specified information from the event, call the  <a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtrender">EvtRender</a> function.

You must call the <a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function to close the handle when done.


#### Examples

For an example that shows how to use this function, see <a href="https://docs.microsoft.com/windows/desktop/WES/rendering-events">Rendering Events</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtrender">EvtRender</a>
 

 

