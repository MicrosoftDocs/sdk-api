---
UID: NS:winuser.tagACCEL
title: tagACCEL
author: windows-sdk-content
description: Defines an accelerator key used in an accelerator table.
old-location: menurc\accel.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators\keyboardacceleratorreference\keyboardacceleratorstructures\accel.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPACCEL, ACCEL, ACCEL structure [Menus and Other Resources], FALT, FCONTROL, FNOINVERT, FSHIFT, FVIRTKEY, LPACCEL, LPACCEL structure pointer [Menus and Other Resources], _win32_ACCEL_str, _win32_accel_str_cpp, menurc.accel, tagACCEL, winui._win32_accel_str, winuser/ACCEL, winuser/LPACCEL"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
req.typenames: ACCEL, *LPACCEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - ACCEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagACCEL structure


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

The accelerator key. This member can be either a <a href="https://msdn.microsoft.com/fa8926ad-41b2-4164-9ba3-ae501fd0eef2">virtual-key code</a> or a character code. 


### -field cmd

Type: <b>WORD</b>

The accelerator identifier. This value is placed in the low-order word of the <i>wParam</i> parameter of the <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> or <a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a> message when the accelerator is pressed. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/cb5e268d-8e38-4682-a736-ecf9bcc34acd">Keyboard Accelerators</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a>



<a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a>
 

 

