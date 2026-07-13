---
UID: NF:commctrl.Header_SetHotDivider
title: Header_SetHotDivider macro (commctrl.h)
description: Changes the color of a divider between header items to indicate the destination of an external drag-and-drop operation. You can use this macro or send the HDM_SETHOTDIVIDER message explicitly.
helpviewer_keywords: ["FALSE","Header_SetHotDivider","Header_SetHotDivider macro [Windows Controls]","TRUE","_win32_Header_SetHotDivider","_win32_Header_SetHotDivider_cpp","commctrl/Header_SetHotDivider","controls.Header_SetHotDivider","controls._win32_Header_SetHotDivider"]
old-location: controls\Header_SetHotDivider.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_sethotdivider.htm
ms.date: 10/21/2024
ms.keywords: FALSE, Header_SetHotDivider, Header_SetHotDivider macro [Windows Controls], TRUE, _win32_Header_SetHotDivider, _win32_Header_SetHotDivider_cpp, commctrl/Header_SetHotDivider, controls.Header_SetHotDivider, controls._win32_Header_SetHotDivider
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Header_SetHotDivider
 - commctrl/Header_SetHotDivider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Header_SetHotDivider
---

# Header_SetHotDivider macro

## -syntax

```cpp
int Header_SetHotDivider(
   HWND  hwnd,
   BOOL  fPos,
   DWORD dw
);
```

## -returns

Type: **int**

Returns the index of the divider that the control highlighted.


## -description

Changes the color of a divider between header items to indicate the destination of an external drag-and-drop operation. You can use this macro or send the <a href="/windows/desktop/Controls/hdm-sethotdivider">HDM_SETHOTDIVIDER</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a header control.

### -param fPos

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A value specifying how <i>dw</i> is to be interpreted. The value in this field can be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that <i>dw</i> holds client coordinates of the pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that <i>dw</i> holds a divider index value.

</td>
</tr>
</table>

### -param dw

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The value held here is interpreted depending on the value of <i>fPos</i>.

If <i>fPos</i> is <b>TRUE</b>, <i>dw</i> represents the x- and y- client coordinates of the pointer. The x-coordinate is in the low word, and the y-coordinate is in the high word. Upon receiving the message, the header control highlights the appropriate divider based on the <i>dw</i> coordinates.

If <i>fPos</i> is <b>FALSE</b>, <i>dw</i> represents the integer index of the divider that will be highlighted.

## -remarks

A header control set to the <a href="/windows/desktop/Controls/header-control-styles">HDS_DRAGDROP</a> style produces this effect automatically. This message is intended to be used when the owner of the control handles drag-and-drop operations manually.
