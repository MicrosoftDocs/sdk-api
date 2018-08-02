---
UID: NF:winevt.EvtFormatMessage
title: EvtFormatMessage function
author: windows-sdk-content
description: Formats a message string.
old-location: wes\evtformatmessage.htm
old-project: WES
ms.assetid: 744fe166-b12c-49d4-ab13-b2ef6a6f9625
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EvtFormatMessage, EvtFormatMessage function [EventLog], wes.evtformatmessage, winevt/EvtFormatMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: EVT_VARIANT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
 - Ext-MS-Win-WevtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtFormatMessage
product: Windows
targetos: Windows
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EvtFormatMessage function


## -description


Formats a message string.


## -parameters




### -param PublisherMetadata [in]

A handle to the provider's metadata that the  <a href="https://msdn.microsoft.com/0839fb15-12a9-4e30-9afa-6f6437956df0">EvtOpenPublisherMetadata</a> function returns. The handle acts as a formatting context for the event or message identifier. 

You can set this parameter to <b>NULL</b> if the Windows Event Collector service forwarded the event. Forwarded events include a <b>RenderingInfo</b> section that contains the rendered message strings. You can also set this parameter to <b>NULL</b> if the event property that you are formatting is defined in the Winmeta.xml file (for example, if level is set to win:Error). In the latter case, the service uses the Winmeta provider as the formatting context and will format only those message strings that you reference in your event that are defined in the Winmeta.xml file.


### -param Event [in]

A handle to an event. The <i>Flags</i> parameter specifies the message string in the event that you want to format. This parameter must be <b>NULL</b> if the <i>Flags</i> parameter is set to <b>EvtFormatMessageId</b>.


### -param MessageId [in]

The resource identifier of the message string that you want to format. To get the resource identifier for a message string, call the <a href="https://msdn.microsoft.com/f85a46ef-873c-4dd9-8b5c-3763fd67fc06">GetPublisherMetadataProperty</a> function. Set this parameter only if the <i>Flags</i> parameter is set to <b>EvtFormatMessageId</b>.


### -param ValueCount [in]

The number of values in the <i>Values</i> parameter.


### -param Values [in]

An array of insertion values to use when formatting the event's message string. Typically, you set this parameter to <b>NULL</b> and the function gets the insertion values from the event data itself. You would use this parameter to override the default behavior and supply the insertion values to use. For example, you might use this parameter if you wanted to resolve a SID to a principal name before inserting the value. 

To override the insertion values, the <i>Flags</i> parameter must be set to <a href="https://msdn.microsoft.com/6a8ed14a-1952-4fcf-ac66-12c1fecd363f">EvtFormatMessageEvent</a>, <a href="https://msdn.microsoft.com/6a8ed14a-1952-4fcf-ac66-12c1fecd363f">EvtFormatMessageXML</a>, or <a href="https://msdn.microsoft.com/6a8ed14a-1952-4fcf-ac66-12c1fecd363f">EvtFormatMessageId</a>. If <i>Flags</i> is set to <a href="https://msdn.microsoft.com/6a8ed14a-1952-4fcf-ac66-12c1fecd363f">EvtFormatMessageId</a>, the resource identifier must identify the event's message string.


### -param Flags [in]

A flag that specifies the message string in the event to format. For possible values, see the <a href="https://msdn.microsoft.com/6a8ed14a-1952-4fcf-ac66-12c1fecd363f">EVT_FORMAT_MESSAGE_FLAGS</a> enumeration.


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
The function failed. Call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.

</td>
</tr>
</table>
 




## -remarks



When the service attempts to find a message for an event, the service looks in the message table resources of the publisher indicated by the <i>PublisherMetadata</i> parameter. After the message ID is found, the following search algorithms are used.



For event messages:

<ol>
<li>Search the file specified in <b>messageFileName</b> attribute of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">provider</a> element.</li>
<li> If not found, search system messages.</li>
</ol>
For the Level, Opcode, and Keyword attributes of the <a href="https://msdn.microsoft.com/61b49e91-afcf-4312-9511-97bf9ceb84df">event</a> element:

<ol>
<li>Search the Winmeta provider resources.</li>
<li>Search the file specified in <b>messageFileName</b> attribute of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">provider</a> element.</li>
</ol>
For the Task attribute of the <a href="https://msdn.microsoft.com/61b49e91-afcf-4312-9511-97bf9ceb84df">event</a> element:

<ol>
<li>Search the file specified in <b>messageFileName</b> attribute of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">provider</a> element.</li>
<li>If not found, search the Winmeta provider resources.</li>
</ol>
For localizable parameters referenced as %%<i>n</i> (where <i>n</i> is the message ID) in the event message:

<ol>
<li>Search files listed in <b>parameterFileName</b> attribute of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">provider</a> element from left to right.</li>
<li>If not found, search system messages.
</li>
</ol>

#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/31dd8276-1925-4a0e-9e2a-6966e8086238">Formatting Event Messages</a> and <a href="https://msdn.microsoft.com/c9442dc1-3599-4e81-a144-943c2843a2f7">Getting a Provider's Metadata</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>
 

 

