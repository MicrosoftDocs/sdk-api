---
UID: NF:winevt.EvtRender
title: EvtRender function (winevt.h)
description: Renders an XML fragment based on the rendering context that you specify.
helpviewer_keywords: ["EvtRender","EvtRender function [EventLog]","wes.evtrender","winevt/EvtRender"]
old-location: wes\evtrender.htm
tech.root: wes
ms.assetid: 521322b6-3424-4321-bcba-fa8dcdc05a76
ms.date: 12/05/2018
ms.keywords: EvtRender, EvtRender function [EventLog], wes.evtrender, winevt/EvtRender
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
 - EvtRender
 - winevt/EvtRender
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
 - EvtRender
---

# EvtRender function


## -description

Renders an XML fragment based on the rendering context that you specify.

## -parameters

### -param Context [in]

A handle to the rendering context that the <a href="/windows/desktop/api/winevt/nf-winevt-evtcreaterendercontext">EvtCreateRenderContext</a> function returns. This parameter must be set to <b>NULL</b> if the <i>Flags</i> parameter is set to EvtRenderEventXml or EvtRenderBookmark.

### -param Fragment [in]

A handle to an event or to a bookmark. Set this parameter to a bookmark handle if the <i>Flags</i> parameter is set to EvtRenderBookmark; otherwise, set to an event handle.

### -param Flags [in]

A flag that identifies what to render. For example, the entire event or specific properties of the event. For possible values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_render_flags">EVT_RENDER_FLAGS</a> enumeration.

### -param BufferSize [in]

The size of the <i>Buffer</i> buffer, in bytes.

### -param Buffer [in]

A caller-allocated buffer that will receive the rendered output. The contents is a <b>null</b>-terminated Unicode string if the <i>Flags</i> parameter is set to EvtRenderEventXml or EvtRenderBookmark. Otherwise, if <i>Flags</i> is set to EvtRenderEventValues, the buffer contains an array of <a href="/windows/desktop/api/winevt/ns-winevt-evt_variant">EVT_VARIANT</a> structures; one for each property specified by the rendering context. The <i>PropertyCount</i> parameter contains the number of elements in the array.

 You can set this parameter to <b>NULL</b> to determine the required buffer size.

### -param BufferUsed [out]

The size, in bytes, of the caller-allocated buffer that the function used or the required buffer size if the function fails with ERROR_INSUFFICIENT_BUFFER.

### -param PropertyCount [out]

The number of the properties in the <i>Buffer</i> parameter if the <i>Flags</i> parameter is set to EvtRenderEventValues; otherwise, zero.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function failed. Call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

</td>
</tr>
</table>

## -remarks

 There is a one-to-one relationship between the array of XPath expressions that you specified when you called the <a href="/windows/desktop/api/winevt/nf-winevt-evtcreaterendercontext">EvtCreateRenderContext</a> function and  the array the values returned in the buffer.

When an EVT_HANDLE from this function is used in the <b>EvtRender</b> function, the list of values that is returned by that function consists of an array of <a href="/windows/desktop/api/winevt/ns-winevt-evt_variant">EVT_VARIANT</a> structures, each corresponding to exactly one of the XPATH expressions in the original <i>ValuePaths</i> parameter array in order of appearance.  Each such <b>EVT_VARIANT</b> structure contains the value that is identified by its corresponding XPATH expression for the event that is being rendered.  If no value is found, the <b>EVT_VARIANT</b> structure contains <b>NULL</b>.  If multiple values are present, the <b>EVT_VARIANT</b> structure will contain the first value encountered.

Be careful when comparing floating-point numbers in XPath queries. Any string representation of a floating-point number is approximated, so the value displayed in XML might not match the number stored with the event. Floating-point numbers should be compared as being less than or greater than a constant.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/rendering-events">Rendering Events</a> and <a href="/windows/desktop/WES/bookmarking-events">Bookmarking Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtcreaterendercontext">EvtCreateRenderContext</a>