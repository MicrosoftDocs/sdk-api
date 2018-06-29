---
UID: NF:winuser.GetClassLongPtrW
title: GetClassLongPtrW function
author: windows-sdk-content
description: Retrieves the specified value from the WNDCLASSEX structure associated with the specified window.
old-location: winmsg\getclasslongptr.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\getclasslongptr.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: GCLP_HBRBACKGROUND, GCLP_HCURSOR, GCLP_HICON, GCLP_HICONSM, GCLP_HMODULE, GCLP_MENUNAME, GCLP_WNDPROC, GCL_CBCLSEXTRA, GCL_CBWNDEXTRA, GCL_STYLE, GCW_ATOM, GetClassLongPtr, GetClassLongPtr function [Windows and Messages], GetClassLongPtrA, GetClassLongPtrW, _win32_GetClassLongPtr, _win32_getclasslongptr_cpp, winmsg.getclasslongptr, winui._win32_getclasslongptr, winuser/GetClassLongPtr, winuser/GetClassLongPtrA, winuser/GetClassLongPtrW
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
req.unicode-ansi: GetClassLongPtrW (Unicode) and GetClassLongPtrA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: POINTER_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-WindowClass-l1-1-2.dll
api_name:
 - GetClassLongPtr
 - GetClassLongPtrA
 - GetClassLongPtrW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetClassLongPtrW function


## -description


Retrieves the specified value from the <a href="https://msdn.microsoft.com/library/ms633577(v=VS.85).aspx">WNDCLASSEX</a> structure associated with the specified window.
<div class="alert"><b>Note</b>  To write code that is compatible with both 32-bit and 64-bit versions of Windows, use <b>GetClassLongPtr</b>. When compiling for 32-bit Windows, <b>GetClassLongPtr</b> is defined as a call to the <a href="https://msdn.microsoft.com/library/ms633580(v=VS.85).aspx">GetClassLong</a> function.</div><div> </div>

## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs. 


### -param nIndex [in]

Type: <b>int</b>

The value to be retrieved. To retrieve a value from the extra class memory, specify the positive, zero-based byte offset of the value to be retrieved. Valid values are in the range zero through the number of bytes of extra class memory, minus eight; for example, if you specified 24 or more bytes of extra class memory, a value of 16 would be an index to the third integer. To retrieve any other value from the <a href="https://msdn.microsoft.com/library/ms633577(v=VS.85).aspx">WNDCLASSEX</a> structure, specify one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GCW_ATOM"></a><a id="gcw_atom"></a><dl>
<dt><b>GCW_ATOM</b></dt>
<dt>-32</dt>
</dl>
</td>
<td width="60%">
Retrieves an 
						<b>ATOM</b> value that uniquely identifies the window class. This is the same atom that the <a href="https://msdn.microsoft.com/library/ms633587(v=VS.85).aspx">RegisterClassEx</a> function returns.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_CBCLSEXTRA"></a><a id="gcl_cbclsextra"></a><dl>
<dt><b>GCL_CBCLSEXTRA</b></dt>
<dt>-20</dt>
</dl>
</td>
<td width="60%">
Retrieves the size, in bytes, of the extra memory associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_CBWNDEXTRA"></a><a id="gcl_cbwndextra"></a><dl>
<dt><b>GCL_CBWNDEXTRA</b></dt>
<dt>-18</dt>
</dl>
</td>
<td width="60%">
Retrieves the size, in bytes, of the extra window memory associated with each window in the class. For information on how to access this memory, see <a href="https://msdn.microsoft.com/library/ms633585(v=VS.85).aspx">GetWindowLongPtr</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GCLP_HBRBACKGROUND"></a><a id="gclp_hbrbackground"></a><dl>
<dt><b>GCLP_HBRBACKGROUND</b></dt>
<dt>-10</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the background brush associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCLP_HCURSOR"></a><a id="gclp_hcursor"></a><dl>
<dt><b>GCLP_HCURSOR</b></dt>
<dt>-12</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the cursor associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCLP_HICON"></a><a id="gclp_hicon"></a><dl>
<dt><b>GCLP_HICON</b></dt>
<dt>-14</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the icon associated with the class.

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
Retrieves a handle to the module that registered the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCLP_MENUNAME"></a><a id="gclp_menuname"></a><dl>
<dt><b>GCLP_MENUNAME</b></dt>
<dt>-8</dt>
</dl>
</td>
<td width="60%">
Retrieves the pointer to the menu name string. The string identifies the menu resource associated with the class.

</td>
</tr>
<tr>
<td width="40%"><a id="GCL_STYLE"></a><a id="gcl_style"></a><dl>
<dt><b>GCL_STYLE</b></dt>
<dt>-26</dt>
</dl>
</td>
<td width="60%">
Retrieves the window-class style bits.

</td>
</tr>
<tr>
<td width="40%"><a id="GCLP_WNDPROC"></a><a id="gclp_wndproc"></a><dl>
<dt><b>GCLP_WNDPROC</b></dt>
<dt>-24</dt>
</dl>
</td>
<td width="60%">
Retrieves the address of the window procedure, or a handle representing the address of the window procedure. You must use the <a href="https://msdn.microsoft.com/library/ms633571(v=VS.85).aspx">CallWindowProc</a> function to call the window procedure. 

</td>
</tr>
</table>
 


## -returns



Type: <strong>Type: <b>ULONG_PTR</b>
</strong>

If the function succeeds, the return value is the requested value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Reserve extra class memory by specifying a nonzero value in the 
				<b>cbClsExtra</b> member of the <a href="https://msdn.microsoft.com/library/ms633577(v=VS.85).aspx">WNDCLASSEX</a> structure used with the <a href="https://msdn.microsoft.com/library/ms633587(v=VS.85).aspx">RegisterClassEx</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms633585(v=VS.85).aspx">GetWindowLongPtr</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms633587(v=VS.85).aspx">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/library/ms633589(v=VS.85).aspx">SetClassLongPtr</a>



<a href="https://msdn.microsoft.com/library/ms633577(v=VS.85).aspx">WNDCLASSEX</a>



<a href="https://msdn.microsoft.com/library/ms632596(v=VS.85).aspx">Window Classes</a>
 

 

