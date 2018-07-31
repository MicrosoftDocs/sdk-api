---
UID: NF:winuser.SetClassLongPtrW
title: SetClassLongPtrW function
author: windows-sdk-content
description: Replaces the specified value at the specified offset in the extra class memory or the WNDCLASSEX structure for the class to which the specified window belongs.
old-location: winmsg\setclasslongptr.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\setclasslongptr.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GCLP_ HBRBACKGROUND, GCLP_HCURSOR, GCLP_HICON, GCLP_HICONSM, GCLP_HMODULE, GCLP_MENUNAME, GCLP_WNDPROC, GCL_CBCLSEXTRA, GCL_CBWNDEXTRA, GCL_STYLE, SetClassLongPtr, SetClassLongPtr function [Windows and Messages], SetClassLongPtrA, SetClassLongPtrW, _win32_SetClassLongPtr, _win32_setclasslongptr_cpp, winmsg.setclasslongptr, winui._win32_setclasslongptr, winuser/SetClassLongPtr, winuser/SetClassLongPtrA, winuser/SetClassLongPtrW
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
req.unicode-ansi: SetClassLongPtrW (Unicode) and SetClassLongPtrA (ANSI)
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
 - Ext-MS-Win-NTUser-WindowClass-l1-1-2.dll
api_name:
 - SetClassLongPtr
 - SetClassLongPtrA
 - SetClassLongPtrW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetClassLongPtrW function


## -description


Replaces the specified value at the specified offset in the extra class memory or the <a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a> structure for the class to which the specified window belongs. <div class="alert"><b>Note</b>  To write code that is compatible with both 32-bit and 64-bit Windows, use <b>SetClassLongPtr</b>. When compiling for 32-bit Windows, <b>SetClassLongPtr</b> is defined as a call to the <a href="https://msdn.microsoft.com/5eed38cf-aaa3-4f31-abfb-ae021352c3bf">SetClassLong</a> function</div>
<div> </div>



## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs. 


### -param nIndex [in]

Type: <b>int</b>

The value to be replaced. To set a value in the extra class memory, specify the positive, zero-based byte offset of the value to be set. Valid values are in the range zero through the number of bytes of extra class memory, minus eight; for example, if you specified 24 or more bytes of extra class memory, a value of 16 would be an index to the third integer. To set a value other than the <a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a> structure, specify one of the following values. 

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
Sets the size, in bytes, of the extra window memory associated with each window in the class. Setting this value does not change the number of extra bytes already allocated. For information on how to access this memory, see <a href="https://msdn.microsoft.com/6c7c4f93-8b6b-403d-a8c7-954d69b37b59">SetWindowLongPtr</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GCLP__HBRBACKGROUND"></a><a id="gclp__hbrbackground"></a><dl>
<dt><b>GCLP_
HBRBACKGROUND</b></dt>
<dt>-10</dt>
</dl>
</td>
<td width="60%">
Replaces a handle to the background brush associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCLP_HCURSOR"></a><a id="gclp_hcursor"></a><dl>
<dt><b>GCLP_HCURSOR</b></dt>
<dt>-12</dt>
</dl>
</td>
<td width="60%">
Replaces a handle to the cursor associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCLP_HICON"></a><a id="gclp_hicon"></a><dl>
<dt><b>GCLP_HICON</b></dt>
<dt>-14</dt>
</dl>
</td>
<td width="60%">
Replaces a handle to the icon associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCLP_HICONSM"></a><a id="gclp_hiconsm"></a><dl>
<dt><b>GCLP_HICONSM</b></dt>
<dt>-34</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the small icon associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCLP_HMODULE"></a><a id="gclp_hmodule"></a><dl>
<dt><b>GCLP_HMODULE</b></dt>
<dt>-16</dt>
</dl>
</td>
<td width="60%">
Replaces a handle to the module that registered the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCLP_MENUNAME"></a><a id="gclp_menuname"></a><dl>
<dt><b>GCLP_MENUNAME</b></dt>
<dt>-8</dt>
</dl>
</td>
<td width="60%">
Replaces the pointer to the menu name string. The string identifies the menu resource associated with the class.

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
<td width="40%"><a id="GCLP_WNDPROC"></a><a id="gclp_wndproc"></a><dl>
<dt><b>GCLP_WNDPROC</b></dt>
<dt>-24</dt>
</dl>
</td>
<td width="60%">
Replaces the pointer to the window procedure associated with the class.

</td>
</tr>
</table>
 


### -param dwNewLong [in]

Type: <b>LONG_PTR</b>

The replacement value. 


## -returns



Type: <strong>Type: <b>ULONG_PTR</b>
</strong>

If the function succeeds, the return value is the previous value of the specified offset. If this was not previously set, the return value is zero. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If you use the <b>SetClassLongPtr</b> function and the <b>GCLP_WNDPROC</b> index to replace the window procedure, the window procedure must conform to the guidelines specified in the description of the <a href="https://msdn.microsoft.com/4bb1cc3d-78db-4546-8ae9-d29fc6ee8f7c">WindowProc</a> callback function. 

Calling <b>SetClassLongPtr</b> with the <b>GCLP_WNDPROC</b> index creates a subclass of the window class that affects all windows subsequently created with the class. An application can subclass a system class, but should not subclass a window class created by another process. 

Reserve extra class memory by specifying a nonzero value in the 
				<b>cbClsExtra</b> member of the <a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a> structure used with the <a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a> function. 

Use the <b>SetClassLongPtr</b> function with care. For example, it is possible to change the background color for a class by using <b>SetClassLongPtr</b>, but this change does not immediately repaint all windows belonging to the class. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/73805362-fd27-458c-ac8f-8ea0cab5f311">GetClassLongPtr</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/6c7c4f93-8b6b-403d-a8c7-954d69b37b59">SetWindowLongPtr</a>



<a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a>



<a href="https://msdn.microsoft.com/6ef633db-af76-42d6-b211-96846578eaac">Window Classes</a>



<a href="https://msdn.microsoft.com/4bb1cc3d-78db-4546-8ae9-d29fc6ee8f7c">WindowProc</a>
 

 

