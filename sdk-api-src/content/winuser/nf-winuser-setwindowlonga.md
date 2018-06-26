---
UID: NF:winuser.SetWindowLongA
title: SetWindowLongA function
author: windows-sdk-content
description: Changes an attribute of the specified window. The function also sets the 32-bit (long) value at the specified offset into the extra window memory.
old-location: winmsg\setwindowlong.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\setwindowlong.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: DWL_DLGPROC, DWL_MSGRESULT, DWL_USER, GWL_EXSTYLE, GWL_HINSTANCE, GWL_ID, GWL_STYLE, GWL_USERDATA, GWL_WNDPROC, SetWindowLong, SetWindowLong function [Windows and Messages], SetWindowLongA, SetWindowLongW, _win32_SetWindowLong, _win32_setwindowlong_cpp, winmsg.setwindowlong, winui._win32_setwindowlong, winuser/SetWindowLong, winuser/SetWindowLongA, winuser/SetWindowLongW
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
req.unicode-ansi: SetWindowLongW (Unicode) and SetWindowLongA (ANSI)
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
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
api_name:
 - SetWindowLong
 - SetWindowLongA
 - SetWindowLongW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetWindowLongA function


## -description


Changes an attribute of the specified window. The function also sets the 32-bit (long) value at the specified offset into the extra window memory.
<div class="alert"><b>Note</b>  This function has been superseded by the <a href="https://msdn.microsoft.com/6c7c4f93-8b6b-403d-a8c7-954d69b37b59">SetWindowLongPtr</a> function. To write code that is compatible with both 32-bit and 64-bit versions of Windows, use the <b>SetWindowLongPtr</b> function.</div><div> </div>

## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs.


### -param nIndex [in]

Type: <b>int</b>

The zero-based offset to the value to be set. Valid values are in the range zero through the number of bytes of extra window memory, minus the size of an integer. To set any other value, specify one of the following values. 

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
Sets a new <a href="https://msdn.microsoft.com/5830B16E-CD52-4a1a-A1BD-3AFE66BA5FDD">extended window style</a>. 

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_HINSTANCE"></a><a id="gwl_hinstance"></a><dl>
<dt><b>GWL_HINSTANCE</b></dt>
<dt>-6</dt>
</dl>
</td>
<td width="60%">
Sets a new application instance handle.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_ID"></a><a id="gwl_id"></a><dl>
<dt><b>GWL_ID</b></dt>
<dt>-12</dt>
</dl>
</td>
<td width="60%">
Sets a new identifier of the child window. The window cannot be a top-level window.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_STYLE"></a><a id="gwl_style"></a><dl>
<dt><b>GWL_STYLE</b></dt>
<dt>-16</dt>
</dl>
</td>
<td width="60%">
Sets a new <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">window style</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_USERDATA"></a><a id="gwl_userdata"></a><dl>
<dt><b>GWL_USERDATA</b></dt>
<dt>-21</dt>
</dl>
</td>
<td width="60%">
Sets the user data associated with the window. This data is intended for use by the application that created the window. Its value is initially zero.

</td>
</tr>
<tr>
<td width="40%"><a id="GWL_WNDPROC"></a><a id="gwl_wndproc"></a><dl>
<dt><b>GWL_WNDPROC</b></dt>
<dt>-4</dt>
</dl>
</td>
<td width="60%">
Sets a new address for the window procedure.


								 You cannot change this attribute if the window does not belong to the same process as the calling thread.

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
Sets the new address of the dialog box procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="DWL_MSGRESULT"></a><a id="dwl_msgresult"></a><dl>
<dt><b>DWL_MSGRESULT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Sets the return value of a message processed in the dialog box procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="DWL_USER"></a><a id="dwl_user"></a><dl>
<dt><b>DWL_USER</b></dt>
<dt>DWLP_DLGPROC + sizeof(DLGPROC)</dt>
</dl>
</td>
<td width="60%">
Sets new extra information that is private to the application, such as handles or pointers.

</td>
</tr>
</table>
 


### -param dwNewLong [in]

Type: <b>LONG</b>

The replacement value. 


## -returns



Type: <strong>Type: <b>LONG</b>
</strong>

If the function succeeds, the return value is the previous value of the specified 32-bit integer.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 

If the previous value of the specified 32-bit integer is zero, and the function succeeds, the return value is zero, but the function does not clear the last error information. This makes it difficult to determine success or failure. To deal with this, you should clear the last error information by calling <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> with 0 before calling <b>SetWindowLong</b>. Then, function failure will be indicated by a return value of zero and a <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> result that is nonzero.




## -remarks



Certain window data is cached, so changes you make using <b>SetWindowLong</b> will not take effect until you call the <a href="https://msdn.microsoft.com/e0a28590-0fed-4ffa-adcd-84b60df316b5">SetWindowPos</a> function. Specifically, if you change any of the frame styles, you must call <b>SetWindowPos</b> with the <b>SWP_FRAMECHANGED</b> flag for the cache to be updated properly. 

If you use <b>SetWindowLong</b> with the <b>GWL_WNDPROC</b> index to replace the window procedure, the window procedure must conform to the guidelines specified in the description of the <a href="https://msdn.microsoft.com/4bb1cc3d-78db-4546-8ae9-d29fc6ee8f7c">WindowProc</a> callback function. 

If you use <b>SetWindowLong</b> with the <b>DWL_MSGRESULT</b> index to set the return value for a message processed by a dialog procedure, you should return <b>TRUE</b> directly afterward. Otherwise, if you call any function that results in your dialog procedure receiving a window message, the nested window message could overwrite the return value you set using <b>DWL_MSGRESULT</b>. 

Calling <b>SetWindowLong</b> with the <b>GWL_WNDPROC</b> index creates a subclass of the window class used to create the window. An application can subclass a system class, but should not subclass a window class created by another process. The <b>SetWindowLong</b> function creates the window subclass by changing the window procedure associated with a particular window class, causing the system to call the new window procedure instead of the previous one. An application must pass any messages not processed by the new window procedure to the previous window procedure by calling <a href="https://msdn.microsoft.com/667449cd-1eea-43de-8268-3da73022d7ac">CallWindowProc</a>. This allows the application to create a chain of window procedures. 

Reserve extra window memory by specifying a nonzero value in the 
				<b>cbWndExtra</b> member of the <a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a> structure used with the <a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a> function. 

You must not call <b>SetWindowLong</b> with the <b>GWL_HWNDPARENT</b> index to change the parent of a child window. Instead, use the <a href="https://msdn.microsoft.com/a13f1cfc-dedc-4190-826f-b29b731e76df">SetParent</a> function. 

If the window has a class style of <b>CS_CLASSDC</b> or <b>CS_OWNDC</b>, do not set the extended window styles <b>WS_EX_COMPOSITED</b> or <b>WS_EX_LAYERED</b>.

Calling <b>SetWindowLong</b> to set the style on a progressbar will reset its position.


#### Examples

For an example, see <a href="using_window_procedures.htm">Subclassing a Window</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/667449cd-1eea-43de-8268-3da73022d7ac">CallWindowProc</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/4c2b634d-1df8-44bb-825c-261eb13045ce">GetWindowLong</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/a13f1cfc-dedc-4190-826f-b29b731e76df">SetParent</a>



<a href="https://msdn.microsoft.com/6c7c4f93-8b6b-403d-a8c7-954d69b37b59">SetWindowLongPtr</a>



<a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a>



<a href="https://msdn.microsoft.com/6ef633db-af76-42d6-b211-96846578eaac">Window Classes</a>



<a href="https://msdn.microsoft.com/4bb1cc3d-78db-4546-8ae9-d29fc6ee8f7c">WindowProc</a>
 

 

