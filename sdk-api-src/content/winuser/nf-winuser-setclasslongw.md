---
UID: NF:winuser.SetClassLongW
title: SetClassLongW function
author: windows-sdk-content
description: Replaces the specified 32-bit (long) value at the specified offset into the extra class memory or the WNDCLASSEX structure for the class to which the specified window belongs.
old-location: winmsg\setclasslong.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\setclasslong.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GCL_CBCLSEXTRA, GCL_CBWNDEXTRA, GCL_HBRBACKGROUND, GCL_HCURSOR, GCL_HICON, GCL_HICONSM, GCL_HMODULE, GCL_MENUNAME, GCL_STYLE, GCL_WNDPROC, SetClassLong, SetClassLong function [Windows and Messages], SetClassLongA, SetClassLongW, _win32_SetClassLong, _win32_setclasslong_cpp, winmsg.setclasslong, winui._win32_setclasslong, winuser/SetClassLong, winuser/SetClassLongA, winuser/SetClassLongW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetClassLongW (Unicode) and SetClassLongA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-WindowClass-l1-1-2.dll
api_name:
 - SetClassLong
 - SetClassLongA
 - SetClassLongW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetClassLongW function


## -description


Replaces the specified 32-bit (<b>long</b>) value at the specified offset into the extra class memory or the <a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a> structure for the class to which the specified window belongs.
			
			
<div class="alert"><b>Note</b>  This function has been superseded by the <a href="https://msdn.microsoft.com/6c9ad727-c81c-4f22-aae6-82d4f0a7dd40">SetClassLongPtr</a> function. To write code that is compatible with both 32-bit and 64-bit versions of Windows, use <b>SetClassLongPtr</b>.
			</div><div> </div>

## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs. 


### -param nIndex [in]

Type: <b>int</b>

The value to be replaced. To set a 32-bit value in the extra class memory, specify the positive, zero-based byte offset of the value to be set. Valid values are in the range zero through the number of bytes of extra class memory, minus four; for example, if you specified 12 or more bytes of extra class memory, a value of 8 would be an index to the third 32-bit integer. To set any other value from the <a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a> structure, specify one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GCL_CBCLSEXTRA"></a><a id="gcl_cbclsextra"></a><dl>
<dt><b>GCL_CBCLSEXTRA</b></dt>
<dt>-20</dt>
</dl>
</td>
<td width="60%">
Sets the size, in bytes, of the extra memory associated with the class. Setting this value does not change the number of extra bytes already allocated.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_CBWNDEXTRA"></a><a id="gcl_cbwndextra"></a><dl>
<dt><b>GCL_CBWNDEXTRA</b></dt>
<dt>-18</dt>
</dl>
</td>
<td width="60%">
Sets the size, in bytes, of the extra window memory associated with each window in the class. Setting this value does not change the number of extra bytes already allocated. For information on how to access this memory, see <a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_HBRBACKGROUND"></a><a id="gcl_hbrbackground"></a><dl>
<dt><b>GCL_HBRBACKGROUND</b></dt>
<dt>-10</dt>
</dl>
</td>
<td width="60%">
Replaces a handle to the background brush associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_HCURSOR"></a><a id="gcl_hcursor"></a><dl>
<dt><b>GCL_HCURSOR</b></dt>
<dt>-12</dt>
</dl>
</td>
<td width="60%">
Replaces a handle to the cursor associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_HICON"></a><a id="gcl_hicon"></a><dl>
<dt><b>GCL_HICON</b></dt>
<dt>-14</dt>
</dl>
</td>
<td width="60%">
Replaces a handle to the icon associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_HICONSM"></a><a id="gcl_hiconsm"></a><dl>
<dt><b>GCL_HICONSM</b></dt>
<dt>-34</dt>
</dl>
</td>
<td width="60%">
Replace a handle to the small icon associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_HMODULE"></a><a id="gcl_hmodule"></a><dl>
<dt><b>GCL_HMODULE</b></dt>
<dt>-16</dt>
</dl>
</td>
<td width="60%">
Replaces a handle to the module that registered the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_MENUNAME"></a><a id="gcl_menuname"></a><dl>
<dt><b>GCL_MENUNAME</b></dt>
<dt>-8</dt>
</dl>
</td>
<td width="60%">
Replaces the address of the menu name string. The string identifies the menu resource associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_STYLE"></a><a id="gcl_style"></a><dl>
<dt><b>GCL_STYLE</b></dt>
<dt>-26</dt>
</dl>
</td>
<td width="60%">
Replaces the window-class style bits.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_WNDPROC"></a><a id="gcl_wndproc"></a><dl>
<dt><b>GCL_WNDPROC</b></dt>
<dt>-24</dt>
</dl>
</td>
<td width="60%">
Replaces the address of the window procedure associated with the class.

</td>
</tr>
</table>
 


### -param dwNewLong [in]

Type: <b>LONG</b>

The replacement value. 


## -returns



Type: <strong>Type: <b>DWORD</b>
</strong>

If the function succeeds, the return value is the previous value of the specified 32-bit integer. If the value was not previously set, the return value is zero. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If you use the <b>SetClassLong</b> function and the <b>GCL_WNDPROC</b> index to replace the window procedure, the window procedure must conform to the guidelines specified in the description of the <a href="https://msdn.microsoft.com/4bb1cc3d-78db-4546-8ae9-d29fc6ee8f7c">WindowProc</a> callback function. 

Calling <b>SetClassLong</b> with the <b>GCL_WNDPROC</b> index creates a subclass of the window class that affects all windows subsequently created with the class. An application can subclass a system class, but should not subclass a window class created by another process. 

Reserve extra class memory by specifying a nonzero value in the <b>cbClsExtra</b> member of the <a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a> structure used with the <a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a> function. 

Use the <b>SetClassLong</b> function with care. For example, it is possible to change the background color for a class by using <b>SetClassLong</b>, but this change does not immediately repaint all windows belonging to the class. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/5021d59a-7aae-4ddc-be66-9abdc75ad316">Displaying an Icon</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8d8e0b2e-635f-4612-8279-a07679c9a144">GetClassLong</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/6c9ad727-c81c-4f22-aae6-82d4f0a7dd40">SetClassLongPtr</a>



<a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a>



<a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a>



<a href="https://msdn.microsoft.com/6ef633db-af76-42d6-b211-96846578eaac">Window Classes</a>



<a href="https://msdn.microsoft.com/4bb1cc3d-78db-4546-8ae9-d29fc6ee8f7c">WindowProc</a>
 

 

