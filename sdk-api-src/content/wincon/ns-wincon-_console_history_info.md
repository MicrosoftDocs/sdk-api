---
UID: NS:wincon._CONSOLE_HISTORY_INFO
title: "_CONSOLE_HISTORY_INFO"
author: windows-driver-content
description: Contains information about the console history.
old-location: consoles\console_history_info.htm
old-project: consoles
ms.assetid: df7d2f12-5299-47ed-b1f6-2db903dba81b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PCONSOLE_HISTORY_INFO, CONSOLE_HISTORY_INFO, CONSOLE_HISTORY_INFO structure [Consoles], HISTORY_NO_DUP_FLAG, PCONSOLE_HISTORY_INFO, PCONSOLE_HISTORY_INFO structure pointer [Consoles], _CONSOLE_HISTORY_INFO, base.console_history_info, consoleapi3/CONSOLE_HISTORY_INFO, consoleapi3/PCONSOLE_HISTORY_INFO, consoles.console_history_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincon.h
req.include-header: Wincon.h
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
req.typenames: CONSOLE_HISTORY_INFO, *PCONSOLE_HISTORY_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	consoleapi3.h
api_name:
-	CONSOLE_HISTORY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CONSOLE_HISTORY_INFO structure


## -description


Contains information about the console history.


## -struct-fields




### -field cbSize

The size of the structure, in bytes. Set this member to <code>sizeof(CONSOLE_HISTORY_INFO)</code>.


### -field HistoryBufferSize

The number of commands kept in each history buffer.


### -field NumberOfHistoryBuffers

The number of history buffers kept for this console process.


### -field dwFlags

This parameter can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HISTORY_NO_DUP_FLAG"></a><a id="history_no_dup_flag"></a><dl>
<dt><b>HISTORY_NO_DUP_FLAG</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Duplicate entries will not be stored in the history buffer.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/145008b3-8a4a-4e6a-9144-ee787ce90ef4">GetConsoleHistoryInfo</a>



<a href="https://msdn.microsoft.com/db180f53-aa3c-4a91-bc3e-9f3f0bb7ab01">SetConsoleHistoryInfo</a>
 

 

