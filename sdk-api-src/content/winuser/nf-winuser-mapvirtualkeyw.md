---
UID: NF:winuser.MapVirtualKeyW
title: MapVirtualKeyW function
author: windows-sdk-content
description: Translates (maps) a virtual-key code into a scan code or character value, or translates a scan code into a virtual-key code.
old-location: inputdev\mapvirtualkey.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\mapvirtualkey.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MAPVK_VK_TO_CHAR, MAPVK_VK_TO_VSC, MAPVK_VSC_TO_VK, MAPVK_VSC_TO_VK_EX, MapVirtualKey, MapVirtualKey function [Keyboard and Mouse Input], MapVirtualKeyA, MapVirtualKeyW, _win32_MapVirtualKey, _win32_mapvirtualkey_cpp, inputdev.mapvirtualkey, winui._win32_mapvirtualkey, winuser/MapVirtualKey, winuser/MapVirtualKeyA, winuser/MapVirtualKeyW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MapVirtualKeyW (Unicode) and MapVirtualKeyA (ANSI)
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
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - api-ms-win-ntuser-ie-keyboard-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - MapVirtualKey
 - MapVirtualKeyA
 - MapVirtualKeyW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# MapVirtualKeyW function


## -description


Translates (maps) a virtual-key code into a scan code or character value, or translates a scan code into a virtual-key code.

To specify a handle to the keyboard layout to use for translating the specified code, use the <a href="https://msdn.microsoft.com/86e09c0d-0067-4b41-b7cf-cf3c3f2e02f7">MapVirtualKeyEx</a> function.


## -parameters




### -param uCode [in]

Type: <b>UINT</b>

The <a href="https://msdn.microsoft.com/fa8926ad-41b2-4164-9ba3-ae501fd0eef2">virtual key code</a> or scan code for a key. How this value is interpreted depends on the value of the <i>uMapType</i> parameter.


### -param uMapType [in]

Type: <b>UINT</b>

The translation to be performed. The value of this parameter depends on the value of the <i>uCode</i> parameter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAPVK_VK_TO_CHAR"></a><a id="mapvk_vk_to_char"></a><dl>
<dt><b>MAPVK_VK_TO_CHAR</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
<i>uCode</i> is a virtual-key code and is translated into an unshifted character value in the low-order word of the return value. Dead keys (diacritics) are indicated by setting the top bit of the return value. If there is no translation, the function returns 0.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPVK_VK_TO_VSC"></a><a id="mapvk_vk_to_vsc"></a><dl>
<dt><b>MAPVK_VK_TO_VSC</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
<i>uCode</i> is a virtual-key code and is translated into a scan code. If it is a virtual-key code that does not distinguish between left- and right-hand keys, the left-hand scan code is returned. If there is no translation, the function returns 0.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPVK_VSC_TO_VK"></a><a id="mapvk_vsc_to_vk"></a><dl>
<dt><b>MAPVK_VSC_TO_VK</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
<i>uCode</i> is a scan code and is translated into a virtual-key code that does not distinguish between left- and right-hand keys. If there is no translation, the function returns 0.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPVK_VSC_TO_VK_EX"></a><a id="mapvk_vsc_to_vk_ex"></a><dl>
<dt><b>MAPVK_VSC_TO_VK_EX</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
<i>uCode</i> is a scan code and is translated into a virtual-key code that distinguishes between left- and right-hand keys. If there is no translation, the function returns 0.

</td>
</tr>
</table>
 


## -returns



Type: <b>UINT</b>

The return value is either a scan code, a virtual-key code, or a character value, depending on the value of <i>uCode</i> and <i>uMapType</i>. If there is no translation, the return value is zero.




## -remarks



An application can use <b>MapVirtualKey</b> to translate scan codes to the virtual-key code constants <b>VK_SHIFT</b>, <b>VK_CONTROL</b>, and <b>VK_MENU</b>, and vice versa. These translations do not distinguish between the left and right instances of the SHIFT, CTRL, or ALT keys.

An application can get the scan code corresponding to the left or right instance of one of these keys by calling <b>MapVirtualKey</b> with <i>uCode</i> set to one of the following virtual-key code constants.

<ul>
<li><b>VK_LSHIFT</b></li>
<li><b>VK_RSHIFT</b></li>
<li><b>VK_LCONTROL</b></li>
<li><b>VK_RCONTROL</b></li>
<li><b>VK_LMENU</b></li>
<li><b>VK_RMENU</b></li>
</ul>
These left- and right-distinguishing constants are available to an application only through the <a href="https://msdn.microsoft.com/d6b31d2c-43b3-4502-a7ed-af564895f27e">GetKeyboardState</a>, <a href="https://msdn.microsoft.com/9c34dd1f-b423-4dcd-b29e-8bf64be57472">SetKeyboardState</a>, <a href="https://msdn.microsoft.com/edc449e4-f37d-4f2c-8add-45b905bd3326">GetAsyncKeyState</a>, <a href="https://msdn.microsoft.com/41c7bcc7-0a14-420c-b338-7ca13c95b7b8">GetKeyState</a>, and <b>MapVirtualKey</b> functions.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/edc449e4-f37d-4f2c-8add-45b905bd3326">GetAsyncKeyState</a>



<a href="https://msdn.microsoft.com/41c7bcc7-0a14-420c-b338-7ca13c95b7b8">GetKeyState</a>



<a href="https://msdn.microsoft.com/d6b31d2c-43b3-4502-a7ed-af564895f27e">GetKeyboardState</a>



<a href="https://msdn.microsoft.com/a3f6ac32-cde9-440d-bbde-0d76b4b5d4a4">Keyboard Input</a>



<a href="https://msdn.microsoft.com/86e09c0d-0067-4b41-b7cf-cf3c3f2e02f7">MapVirtualKeyEx</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/9c34dd1f-b423-4dcd-b29e-8bf64be57472">SetKeyboardState</a>
 

 

