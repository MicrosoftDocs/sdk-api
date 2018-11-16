---
UID: NF:winuser.GetWindowLongW
title: GetWindowLongW function
author: windows-sdk-content
description: Retrieves information about the specified window.
old-location: winmsg\getwindowlong.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\getwindowlong.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DWL_DLGPROC, DWL_MSGRESULT, DWL_USER, GWL_EXSTYLE, GWL_HINSTANCE, GWL_HWNDPARENT, GWL_ID, GWL_STYLE, GWL_USERDATA, GWL_WNDPROC, GetWindowLong, GetWindowLong function [Windows and Messages], GetWindowLongA, GetWindowLongW, _win32_GetWindowLong, _win32_getwindowlong_cpp, winmsg.getwindowlong, winui._win32_getwindowlong, winuser/GetWindowLong, winuser/GetWindowLongA, winuser/GetWindowLongW
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
req.unicode-ansi: GetWindowLongW (Unicode) and GetWindowLongA (ANSI)
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
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
api_name:
 - GetWindowLong
 - GetWindowLongA
 - GetWindowLongW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetWindowLongW
: 
---

# GetWindowLongW function


## -description


Retrieves information about the specified window. The function also retrieves the 32-bit (<b>DWORD</b>) value at the specified offset into the extra window memory. <div class="alert"><b>Note</b>  If you are retrieving a pointer or a handle, this function has been superseded by the <a href="https://msdn.microsoft.com/en-us/library/ms633585(v=VS.85).aspx">GetWindowLongPtr</a> function. (Pointers and handles are 32 bits on 32-bit Windows and 64 bits on 64-bit Windows.) To write code that is compatible with both 32-bit and 64-bit versions of Windows, use <b>GetWindowLongPtr</b>.</div>
<div> </div>



## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs. 


### -param nIndex [in]

Type: <b>int</b>

The zero-based offset to the value to be retrieved. Valid values are in the range zero through the number of bytes of extra window memory, minus four; for example, if you specified 12 or more bytes of extra memory, a value of 8 would be an index to the third 32-bit integer. To retrieve any other value, specify one of the following values.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GWL_EXSTYLE"></a><a id="gwl_exstyle"></a><dl>
<dt><b>GWL_EXSTYLE</b></dt>
<dt>-20</dt>
</dl>
</td>
<td width="60%">
Retrieves the <a href="https://msdn.microsoft.com/5830B16E-CD52-4a1a-A1BD-3AFE66BA5FDD">extended window styles</a>. 

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_HINSTANCE"></a><a id="gwl_hinstance"></a><dl>
<dt><b>GWL_HINSTANCE</b></dt>
<dt>-6</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the application instance.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_HWNDPARENT"></a><a id="gwl_hwndparent"></a><dl>
<dt><b>GWL_HWNDPARENT</b></dt>
<dt>-8</dt>
</dl>
</td>
<td width="60%">
Retrieves a handle to the parent window, if any.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_ID"></a><a id="gwl_id"></a><dl>
<dt><b>GWL_ID</b></dt>
<dt>-12</dt>
</dl>
</td>
<td width="60%">
Retrieves the identifier of the window.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_STYLE"></a><a id="gwl_style"></a><dl>
<dt><b>GWL_STYLE</b></dt>
<dt>-16</dt>
</dl>
</td>
<td width="60%">
Retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms632600(v=VS.85).aspx">window styles</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_USERDATA"></a><a id="gwl_userdata"></a><dl>
<dt><b>GWL_USERDATA</b></dt>
<dt>-21</dt>
</dl>
</td>
<td width="60%">
Retrieves the user data associated with the window. This data is intended for use by the application that created the window. Its value is initially zero.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_WNDPROC"></a><a id="gwl_wndproc"></a><dl>
<dt><b>GWL_WNDPROC</b></dt>
<dt>-4</dt>
</dl>
</td>
<td width="60%">
Retrieves the address of the window procedure, or a handle representing the address of the window procedure. You must use the <a href="https://msdn.microsoft.com/en-us/library/ms633571(v=VS.85).aspx">CallWindowProc</a> function to call the window procedure.

</td>
</tr>
</table>
 


The following values are also available when the <i>hWnd</i> parameter identifies a dialog box.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DWL_DLGPROC"></a><a id="dwl_dlgproc"></a><dl>
<dt><b>DWL_DLGPROC</b></dt>
<dt>DWLP_MSGRESULT + sizeof(LRESULT)</dt>
</dl>
</td>
<td width="60%">
Retrieves the address of the dialog box procedure, or a handle representing the address of the dialog box procedure. You must use the <a href="https://msdn.microsoft.com/en-us/library/ms633571(v=VS.85).aspx">CallWindowProc</a> function to call the dialog box procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="DWL_MSGRESULT"></a><a id="dwl_msgresult"></a><dl>
<dt><b>DWL_MSGRESULT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Retrieves the return value of a message processed in the dialog box procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="DWL_USER"></a><a id="dwl_user"></a><dl>
<dt><b>DWL_USER</b></dt>
<dt>DWLP_DLGPROC + sizeof(DLGPROC)</dt>
</dl>
</td>
<td width="60%">
Retrieves extra information private to the application, such as handles or pointers.

</td>
</tr>
</table>
 


## -returns



Type: <strong>Type: <b>LONG</b>
</strong>

If the function succeeds, the return value is the requested value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 

If <a href="https://msdn.microsoft.com/en-us/library/ms633591(v=VS.85).aspx">SetWindowLong</a> has not been called previously, <b>GetWindowLong</b> returns zero for values in the extra window or class memory.




## -remarks



Reserve extra window memory by specifying a nonzero value in the 
				<b>cbWndExtra</b> member of the <a href="https://msdn.microsoft.com/en-us/library/ms633577(v=VS.85).aspx">WNDCLASSEX</a> structure used with the <a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a> function. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms632598(v=VS.85).aspx">Creating, Enumerating, and Sizing Child Windows</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms633571(v=VS.85).aspx">CallWindowProc</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633585(v=VS.85).aspx">GetWindowLongPtr</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633541(v=VS.85).aspx">SetParent</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633591(v=VS.85).aspx">SetWindowLong</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633576(v=VS.85).aspx">WNDCLASS</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632596(v=VS.85).aspx">Window Classes</a>
 

 

