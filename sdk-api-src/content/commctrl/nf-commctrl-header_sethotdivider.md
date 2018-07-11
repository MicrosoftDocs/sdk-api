---
UID: NF:commctrl.Header_SetHotDivider
title: Header_SetHotDivider macro
author: windows-sdk-content
description: Changes the color of a divider between header items to indicate the destination of an external drag-and-drop operation. You can use this macro or send the HDM_SETHOTDIVIDER message explicitly.
old-location: controls\Header_SetHotDivider.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\header\macros\header_sethotdivider.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: FALSE, Header_SetHotDivider, Header_SetHotDivider macro [Windows Controls], TRUE, _win32_Header_SetHotDivider, _win32_Header_SetHotDivider_cpp, commctrl/Header_SetHotDivider, controls.Header_SetHotDivider, controls._win32_Header_SetHotDivider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Header_SetHotDivider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# Header_SetHotDivider macro


## -description


Changes the color of a divider between header items to indicate the destination of an external drag-and-drop operation. You can use this macro or send the <a href="https://msdn.microsoft.com/56f6e5c6-1df3-4b4d-9ad8-97fb168c5462">HDM_SETHOTDIVIDER</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param fPos

TBD


### -param dw

TBD






#### - dwInputValue

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The value held here is interpreted depending on the value of 
					<i>flag</i>. 

If 
						<i>flag</i> is <b>TRUE</b>, 
						<i>dwInputValue</i> represents the x- and y- client coordinates of the pointer. The x-coordinate is in the low word, and the y-coordinate is in the high word. Upon receiving the message, the header control highlights the appropriate divider based on the 
						<i>dwInputValue</i> coordinates. 

If 
						<i>flag</i> is <b>FALSE</b>, 
						<i>dwInputValue</i> represents the integer index of the divider that will be highlighted. 


#### - flag

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A value specifying how 
					<i>dwInputValue</i> is to be interpreted. The value in this field can be one of the following: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
Indicates that 
						<i>dwInputValue</i> holds client coordinates of the pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Indicates that 
						<i>dwInputValue</i> holds a divider index value.

</td>
</tr>
</table>
 


#### - hwndHD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a header control. 


## -remarks



A header control set to the <a href="Header_Control_Styles.htm">HDS_DRAGDROP</a> style produces this effect automatically. This message is intended to be used when the owner of the control handles drag-and-drop operations manually. 



