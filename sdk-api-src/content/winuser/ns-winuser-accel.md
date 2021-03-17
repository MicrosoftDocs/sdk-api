---
UID: NS:winuser.tagACCEL
title: ACCEL (winuser.h)
description: Defines an accelerator key used in an accelerator table.
helpviewer_keywords: ["*LPACCEL","ACCEL","ACCEL structure [Menus and Other Resources]","FALT","FCONTROL","FNOINVERT","FSHIFT","FVIRTKEY","LPACCEL","LPACCEL structure pointer [Menus and Other Resources]","_win32_ACCEL_str","_win32_accel_str_cpp","menurc.accel","winui._win32_accel_str","winuser/ACCEL","winuser/LPACCEL"]
old-location: menurc\accel.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators\keyboardacceleratorreference\keyboardacceleratorstructures\accel.htm
ms.date: 12/05/2018
ms.keywords: '*LPACCEL, ACCEL, ACCEL structure [Menus and Other Resources], FALT, FCONTROL, FNOINVERT, FSHIFT, FVIRTKEY, LPACCEL, LPACCEL structure pointer [Menus and Other Resources], _win32_ACCEL_str, _win32_accel_str_cpp, menurc.accel, winui._win32_accel_str, winuser/ACCEL, winuser/LPACCEL'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ACCEL, *LPACCEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagACCEL
 - winuser/tagACCEL
 - LPACCEL
 - winuser/LPACCEL
 - ACCEL
 - winuser/ACCEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - ACCEL
---

# ACCEL structure


## -description

Defines an accelerator key used in an accelerator table.

## -struct-fields

### -field fVirt

Type: <b>BYTE</b>

The accelerator behavior. This member can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FALT"></a><a id="falt"></a><dl>
<dt><b>FALT</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
The ALT key must be held down when the accelerator key is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="FCONTROL"></a><a id="fcontrol"></a><dl>
<dt><b>FCONTROL</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
The CTRL key must be held down when the accelerator key is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="FNOINVERT"></a><a id="fnoinvert"></a><dl>
<dt><b>FNOINVERT</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
No top-level menu item is highlighted when the accelerator is used. If this flag is not specified, a top-level menu item will be highlighted, if possible, when the accelerator is used. This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows. 

</td>
</tr>
<tr>
<td width="40%"><a id="FSHIFT"></a><a id="fshift"></a><dl>
<dt><b>FSHIFT</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
The SHIFT key must be held down when the accelerator key is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="FVIRTKEY"></a><a id="fvirtkey"></a><dl>
<dt><b>FVIRTKEY</b></dt>
<dt>TRUE</dt>
</dl>
</td>
<td width="60%">
The <b>key</b> member specifies a virtual-key code. If this flag is not specified, <b>key</b> is assumed to specify a character code.

</td>
</tr>
</table>

### -field key

Type: <b>WORD</b>

The accelerator key. This member can be either a <a href="/windows/desktop/inputdev/virtual-key-codes">virtual-key code</a> or a character code.

### -field cmd

Type: <b>WORD</b>

The accelerator identifier. This value is placed in the low-order word of the <i>wParam</i> parameter of the <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> or <a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a> message when the accelerator is pressed.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/menurc/keyboard-accelerators">Keyboard Accelerators</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a>



<a href="/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a>