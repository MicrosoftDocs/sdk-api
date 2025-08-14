---
UID: NF:winevt.EvtFormatMessage
title: EvtFormatMessage function (winevt.h)
description: Formats a message string. (EvtFormatMessage)
helpviewer_keywords: ["EvtFormatMessage","EvtFormatMessage function [EventLog]","wes.evtformatmessage","winevt/EvtFormatMessage"]
old-location: wes\evtformatmessage.htm
tech.root: wes
ms.assetid: 744fe166-b12c-49d4-ab13-b2ef6a6f9625
ms.date: 12/05/2018
ms.keywords: EvtFormatMessage, EvtFormatMessage function [EventLog], wes.evtformatmessage, winevt/EvtFormatMessage
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
 - EvtFormatMessage
 - winevt/EvtFormatMessage
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
 - Ext-MS-Win-WevtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtFormatMessage
---

# EvtFormatMessage function


## -description

Formats a message string.

## -parameters

### -param PublisherMetadata [in]

A handle to the provider's metadata that the  <a href="/windows/desktop/api/winevt/nf-winevt-evtopenpublishermetadata">EvtOpenPublisherMetadata</a> function returns. The handle acts as a formatting context for the event or message identifier. 

You can set this parameter to <b>NULL</b> if the Windows Event Collector service forwarded the event. Forwarded events include a <b>RenderingInfo</b> section that contains the rendered message strings. You can also set this parameter to <b>NULL</b> if the event property that you are formatting is defined in the Winmeta.xml file (for example, if level is set to win:Error). In the latter case, the service uses the Winmeta provider as the formatting context and will format only those message strings that you reference in your event that are defined in the Winmeta.xml file.

### -param Event [in]

A handle to an event. The <i>Flags</i> parameter specifies the message string in the event that you want to format. This parameter must be <b>NULL</b> if the <i>Flags</i> parameter is set to <b>EvtFormatMessageId</b>.

### -param MessageId [in]

The resource identifier of the message string that you want to format. To get the resource identifier for a message string, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtgetpublishermetadataproperty">GetPublisherMetadataProperty</a> function. Set this parameter only if the <i>Flags</i> parameter is set to <b>EvtFormatMessageId</b>.

### -param ValueCount [in]

The number of values in the <i>Values</i> parameter.

### -param Values [in]

An array of insertion values to use when formatting the event's message string. Typically, you set this parameter to <b>NULL</b> and the function gets the insertion values from the event data itself. You would use this parameter to override the default behavior and supply the insertion values to use. For example, you might use this parameter if you wanted to resolve a SID to a principal name before inserting the value. 

To override the insertion values, the <i>Flags</i> parameter must be set to <a href="/windows/desktop/api/winevt/ne-winevt-evt_format_message_flags">EvtFormatMessageEvent</a>, <a href="/windows/desktop/api/winevt/ne-winevt-evt_format_message_flags">EvtFormatMessageXML</a>, or <a href="/windows/desktop/api/winevt/ne-winevt-evt_format_message_flags">EvtFormatMessageId</a>. If <i>Flags</i> is set to <a href="/windows/desktop/api/winevt/ne-winevt-evt_format_message_flags">EvtFormatMessageId</a>, the resource identifier must identify the event's message string.

### -param Flags [in]

A flag that specifies the message string in the event to format. For possible values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_format_message_flags">EVT_FORMAT_MESSAGE_FLAGS</a> enumeration.

### -param BufferSize [in]

The size of the <i>Buffer</i> buffer, in characters.

### -param Buffer [in]

A caller-allocated buffer that will receive the formatted message string. You can set this parameter to <b>NULL</b> to determine the required buffer size.

### -param BufferUsed [out]

The size, in characters of the caller-allocated buffer that the function used or the required buffer size if the function fails with ERROR_INSUFFICIENT_BUFFER.

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

When the service attempts to find a message for an event, the service looks in the message table resources of the publisher indicated by the <i>PublisherMetadata</i> parameter. After the message ID is found, the following search algorithms are used.



For event messages:

<ol>
<li>Search the file specified in <b>messageFileName</b> attribute of the <a href="/windows/desktop/WES/eventmanifestschema-provider-eventstype-element">provider</a> element.</li>
<li> If not found, search system messages.</li>
</ol>
For the Level, Opcode, and Keyword attributes of the <a href="/windows/desktop/WES/eventmanifestschema-event-definitiontype-element">event</a> element:

<ol>
<li>Search the Winmeta provider resources.</li>
<li>Search the file specified in <b>messageFileName</b> attribute of the <a href="/windows/desktop/WES/eventmanifestschema-provider-eventstype-element">provider</a> element.</li>
</ol>
For the Task attribute of the <a href="/windows/desktop/WES/eventmanifestschema-event-definitiontype-element">event</a> element:

<ol>
<li>Search the file specified in <b>messageFileName</b> attribute of the <a href="/windows/desktop/WES/eventmanifestschema-provider-eventstype-element">provider</a> element.</li>
<li>If not found, search the Winmeta provider resources.</li>
</ol>
For localizable parameters referenced as %%<i>n</i> (where <i>n</i> is the message ID) in the event message:

<ol>
<li>Search files listed in <b>parameterFileName</b> attribute of the <a href="/windows/desktop/WES/eventmanifestschema-provider-eventstype-element">provider</a> element from left to right.</li>
<li>If not found, search system messages.
</li>
</ol>

#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/formatting-event-messages">Formatting Event Messages</a> and <a href="/windows/desktop/WES/getting-a-provider-s-metadata-">Getting a Provider's Metadata</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>
