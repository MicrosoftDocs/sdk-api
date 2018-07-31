---
UID: NF:winuser.GetKeyboardType
title: GetKeyboardType function
author: windows-sdk-content
description: Retrieves information about the current keyboard.
old-location: inputdev\getkeyboardtype.htm
old-project: inputdev
ms.assetid: 39b9ba8b-0cab-465c-9a58-2b69eea7de76
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetKeyboardType, GetKeyboardType function [Keyboard and Mouse Input], _win32_getkeyboardtype, base.getkeyboardtype, inputdev.getkeyboardtype, winui.getkeyboardtype, winuser/GetKeyboardType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-1-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - GetKeyboardType
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetKeyboardType function


## -description


Retrieves information about the current keyboard.


## -parameters




### -param nTypeFlag [in]

Type: <b>int</b>

The type of keyboard information to be retrieved. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Keyboard type

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Keyboard subtype

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The number of function keys on the keyboard

</td>
</tr>
</table>
 


## -returns



Type: <b>int</b>

If the function succeeds, the return value specifies the requested information.

If the function fails and <i>nTypeFlag</i> is not one, the return value is zero; zero is a valid return value when <i>nTypeFlag</i> is one (keyboard subtype). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The type may be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
1

</td>
<td>
IBM PC/XT or compatible (83-key) keyboard

</td>
</tr>
<tr>
<td>
2

</td>
<td>
Olivetti "ICO" (102-key) keyboard

</td>
</tr>
<tr>
<td>
3

</td>
<td>
IBM PC/AT (84-key) or similar keyboard

</td>
</tr>
<tr>
<td>
4

</td>
<td>
IBM enhanced (101- or 102-key) keyboard

</td>
</tr>
<tr>
<td>
5

</td>
<td>
Nokia 1050 and similar keyboards

</td>
</tr>
<tr>
<td>
6

</td>
<td>
Nokia 9140 and similar keyboards

</td>
</tr>
<tr>
<td>
7

</td>
<td>
Japanese keyboard

</td>
</tr>
</table>
 

The subtype is an original equipment manufacturer (OEM)-dependent value.

The application can also determine the number of function keys on a keyboard from the keyboard type. Following are the number of function keys for each keyboard type.

<table>
<tr>
<th>Type</th>
<th>Number of function keys</th>
</tr>
<tr>
<td>
1

</td>
<td>
10

</td>
</tr>
<tr>
<td>
2

</td>
<td>
12 (sometimes 18)

</td>
</tr>
<tr>
<td>
3

</td>
<td>
10

</td>
</tr>
<tr>
<td>
4

</td>
<td>
12

</td>
</tr>
<tr>
<td>
5

</td>
<td>
10

</td>
</tr>
<tr>
<td>
6

</td>
<td>
24

</td>
</tr>
<tr>
<td>
7

</td>
<td>
Hardware dependent and specified by the OEM

</td>
</tr>
</table>
 

When a single USB keyboard is connected to the computer, this function returns the code 81.




## -see-also




<a href="https://msdn.microsoft.com/731b8209-1ca8-4667-bd39-7bd0cef45380">Keyboard Input Functions</a>
 

 

