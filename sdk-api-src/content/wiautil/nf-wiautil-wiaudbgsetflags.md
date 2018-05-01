---
UID: NF:wiautil.wiauDbgSetFlags
title: wiauDbgSetFlags function
author: windows-driver-content
description: The wiauDbgSetFlags function sets debugging flags.
old-location: image\wiaudbgsetflags.htm
old-project: image
ms.assetid: e3b944ef-daa5-412c-ac11-7b08d2b9333b
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: image.wiaudbgsetflags, wiauDbgSetFlags, wiauDbgSetFlags function [Imaging Devices], wiauFncs_d0f9a6a3-6958-44cb-9467-7f6413f95ca7.xml, wiautil/wiauDbgSetFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wiautil.h
req.include-header: Wiautil.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SKIP_AMOUNT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wiautil.h
api_name:
-	wiauDbgSetFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# wiauDbgSetFlags function


## -description


The <b>wiauDbgSetFlags</b> function sets debugging flags.


## -parameters




### -param flags

Is a set of flags that control message logging. This parameter can be set to a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
WIAUDBG_BREAK_ON_ERRORS

</td>
<td>
Call <b>DebugBreak</b> (described in the Microsoft Windows SDK documentation) when an error occurs.

</td>
</tr>
<tr>
<td>
WIAUDBG_DONT_LOG

</td>
<td>
Do not log to either log file or debugger.

</td>
</tr>
<tr>
<td>
WIAUDBG_DONT_LOG_TO_DEBUGGER

</td>
<td>
Do not log to debugger.

</td>
</tr>
<tr>
<td>
WIAUDBG_DONT_LOG_TO_FILE

</td>
<td>
Do not log to log file.

</td>
</tr>
<tr>
<td>
WIAUDBG_DUMP

</td>
<td>
Log data.

</td>
</tr>
<tr>
<td>
WIAUDBG_ERRORS

</td>
<td>
Log error messages.

</td>
</tr>
<tr>
<td>
WIAUDBG_FNS

</td>
<td>
Log function entries and exits.

</td>
</tr>
<tr>
<td>
WIAUDBG_PRINT_INFO

</td>
<td>
Log thread, file, and line number.

</td>
</tr>
<tr>
<td>
WIAUDBG_PRINT_TIME

</td>
<td>
Log current time.

</td>
</tr>
<tr>
<td>
WIAUDBG_TRACES

</td>
<td>
Log trace messages.

</td>
</tr>
<tr>
<td>
WIAUDBG_WARNINGS

</td>
<td>
Log warning messages.

</td>
</tr>
</table>
 


## -returns



The <b>wiauDbgSetFlags</b> function returns a value containing the flags that were in effect before the call to this function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549643">wiauDbgFlags</a>
 

 

