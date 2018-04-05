---
UID: NS:wincon._WINDOW_BUFFER_SIZE_RECORD
title: "_WINDOW_BUFFER_SIZE_RECORD"
author: windows-driver-content
description: Describes a change in the size of the console screen buffer.
old-location: consoles\window_buffer_size_record_str.htm
old-project: consoles
ms.assetid: 2f2875e8-aa09-455b-a923-7cc388525b98
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINDOW_BUFFER_SIZE_RECORD, WINDOW_BUFFER_SIZE_RECORD, WINDOW_BUFFER_SIZE_RECORD structure [Consoles], _WINDOW_BUFFER_SIZE_RECORD, _win32_window_buffer_size_record_str, base.window_buffer_size_record_str, consoles.window_buffer_size_record_str, wincon/WINDOW_BUFFER_SIZE_RECORD"
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
req.typenames: WINDOW_BUFFER_SIZE_RECORD, *PWINDOW_BUFFER_SIZE_RECORD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincon.h
api_name:
-	WINDOW_BUFFER_SIZE_RECORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINDOW_BUFFER_SIZE_RECORD structure


## -description


Describes a change in the size of the console screen buffer.


## -struct-fields




### -field dwSize

A 
<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure that contains the size of the console screen buffer, in character cell columns and rows.


## -remarks



Buffer size events are placed in the input buffer when the console is in window-aware mode (<b>ENABLE_WINDOW_INPUT</b>).


#### Examples

For an example, see <a href="https://msdn.microsoft.com/57570f3b-4a37-4789-bf6c-474fae60171d">Reading Input Buffer Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a>



<a href="https://msdn.microsoft.com/a46ba7fd-097a-455d-96ac-13aa01e11dc1">INPUT_RECORD</a>



<a href="https://msdn.microsoft.com/5a9f7b18-cdea-4041-a377-5532d30e0105">ReadConsoleInput</a>
 

 

