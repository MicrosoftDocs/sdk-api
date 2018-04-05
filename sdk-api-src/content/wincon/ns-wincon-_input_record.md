---
UID: NS:wincon._INPUT_RECORD
title: "_INPUT_RECORD"
author: windows-driver-content
description: Describes an input event in the console input buffer.
old-location: consoles\input_record_str.htm
old-project: consoles
ms.assetid: a46ba7fd-097a-455d-96ac-13aa01e11dc1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PINPUT_RECORD, FOCUS_EVENT, INPUT_RECORD, INPUT_RECORD structure [Consoles], KEY_EVENT, MENU_EVENT, MOUSE_EVENT, WINDOW_BUFFER_SIZE_EVENT, _INPUT_RECORD, _win32_input_record_str, base.input_record_str, consoles.input_record_str, wincon/INPUT_RECORD"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincon.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: INPUT_RECORD, *PINPUT_RECORD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincon.h
api_name:
-	INPUT_RECORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _INPUT_RECORD structure


## -description


Describes an input event in the console input buffer. These records can be read from the input buffer by using the 
<a href="https://msdn.microsoft.com/5a9f7b18-cdea-4041-a377-5532d30e0105">ReadConsoleInput</a> or 
<a href="https://msdn.microsoft.com/9982dc20-43bd-4ee3-a68d-157c9134daca">PeekConsoleInput</a> function, or written to the input buffer by using the 
<a href="https://msdn.microsoft.com/ad06231f-5063-4aff-b14d-8df5e6e42430">WriteConsoleInput</a> function.


## -struct-fields




### -field Event

The event information. The format of this member depends on the event type specified by the <b>EventType</b> member.


### -field EventType

A handle to the type of input event and the event record stored in the <b>Event</b> member. 




This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FOCUS_EVENT"></a><a id="focus_event"></a><dl>
<dt><b>FOCUS_EVENT</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The <b>Event</b> member contains a 
<a href="https://msdn.microsoft.com/4db0ae89-8446-4f0a-98e2-ba0b11ef7efe">FOCUS_EVENT_RECORD</a> structure. These events are used internally and should be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="KEY_EVENT"></a><a id="key_event"></a><dl>
<dt><b>KEY_EVENT</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The <b>Event</b> member contains a 
<a href="https://msdn.microsoft.com/b3fed86b-84ef-48e4-97e1-cb3d65f714a7">KEY_EVENT_RECORD</a> structure with information about a keyboard event.

</td>
</tr>
<tr>
<td width="40%"><a id="MENU_EVENT"></a><a id="menu_event"></a><dl>
<dt><b>MENU_EVENT</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The <b>Event</b> member contains a 
<a href="https://msdn.microsoft.com/7efef0e0-01ba-44ba-a972-25c6b3aed2bd">MENU_EVENT_RECORD</a> structure. These events are used internally and should be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="MOUSE_EVENT"></a><a id="mouse_event"></a><dl>
<dt><b>MOUSE_EVENT</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The <b>Event</b> member contains a 
<a href="https://msdn.microsoft.com/84ea54c6-8872-4111-8d72-1377409b9247">MOUSE_EVENT_RECORD</a> structure with information about a mouse movement or button press event.

</td>
</tr>
<tr>
<td width="40%"><a id="WINDOW_BUFFER_SIZE_EVENT"></a><a id="window_buffer_size_event"></a><dl>
<dt><b>WINDOW_BUFFER_SIZE_EVENT</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The <b>Event</b> member contains a 
<a href="https://msdn.microsoft.com/2f2875e8-aa09-455b-a923-7cc388525b98">WINDOW_BUFFER_SIZE_RECORD</a> structure with information about the new size of the console screen buffer.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/4db0ae89-8446-4f0a-98e2-ba0b11ef7efe">FOCUS_EVENT_RECORD</a>



<a href="https://msdn.microsoft.com/b3fed86b-84ef-48e4-97e1-cb3d65f714a7">KEY_EVENT_RECORD</a>



<a href="https://msdn.microsoft.com/7efef0e0-01ba-44ba-a972-25c6b3aed2bd">MENU_EVENT_RECORD</a>



<a href="https://msdn.microsoft.com/84ea54c6-8872-4111-8d72-1377409b9247">MOUSE_EVENT_RECORD</a>



<a href="https://msdn.microsoft.com/9982dc20-43bd-4ee3-a68d-157c9134daca">PeekConsoleInput</a>



<a href="https://msdn.microsoft.com/5a9f7b18-cdea-4041-a377-5532d30e0105">ReadConsoleInput</a>



<a href="https://msdn.microsoft.com/ad06231f-5063-4aff-b14d-8df5e6e42430">WriteConsoleInput</a>
 

 

