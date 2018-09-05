---
UID: NF:winuser.SetWindowLongPtrA
title: SetWindowLongPtrA function
author: windows-sdk-content
description: Changes an attribute of the specified window.
old-location: winmsg\setwindowlongptr.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassfunctions\setwindowlongptr.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DWLP_DLGPROC, DWLP_MSGRESULT, DWLP_USER, GWLP_HINSTANCE, GWLP_ID, GWLP_USERDATA, GWLP_WNDPROC, GWL_EXSTYLE, GWL_STYLE, SetWindowLongPtr, SetWindowLongPtr function [Windows and Messages], SetWindowLongPtrA, SetWindowLongPtrW, _win32_SetWindowLongPtr, _win32_setwindowlongptr_cpp, winmsg.setwindowlongptr, winui._win32_setwindowlongptr, winuser/SetWindowLongPtr, winuser/SetWindowLongPtrA, winuser/SetWindowLongPtrW
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
req.unicode-ansi: SetWindowLongPtrW (Unicode) and SetWindowLongPtrA (ANSI)
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
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowclass-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
api_name:
 - SetWindowLongPtr
 - SetWindowLongPtrA
 - SetWindowLongPtrW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetWindowLongPtrA function


## -description


Changes an attribute of the specified window. The function also sets a value at the specified offset in the extra window memory. <div class="alert"><b>Note</b>  To write code that is compatible with both 32-bit and 64-bit versions of Windows, use <b>SetWindowLongPtr</b>. When compiling for 32-bit Windows, <b>SetWindowLongPtr</b> is defined as a call to the <a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a> function.</div>
<div> </div>



## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window and, indirectly, the class to which the window belongs. The <b>SetWindowLongPtr</b> function fails if the process that owns the window specified by the <i>hWnd</i> parameter is at a higher process privilege in the UIPI hierarchy than the process the calling thread resides in.

<b>Windows XP/2000:  </b> The <b>SetWindowLongPtr</b> function fails if the window specified by the <i>hWnd</i> parameter does not belong to the same process as the calling thread.


### -param nIndex [in]

Type: <b>int</b>

The zero-based offset to the value to be set. Valid values are in the range zero through the number of bytes of extra window memory, minus the size of a <b>LONG_PTR</b>. To set any other value, specify one of the following values.

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
<td width="40%"><a id="GWLP_HINSTANCE"></a><a id="gwlp_hinstance"></a><dl>
<dt><b>GWLP_HINSTANCE</b></dt>
<dt>-6</dt>
</dl>
</td>
<td width="60%">
Sets a new application instance handle.

</td>
</tr>
<tr>
<td width="40%"><a id="GWLP_ID"></a><a id="gwlp_id"></a><dl>
<dt><b>GWLP_ID</b></dt>
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
<td width="40%"><a id="GWLP_USERDATA"></a><a id="gwlp_userdata"></a><dl>
<dt><b>GWLP_USERDATA</b></dt>
<dt>-21</dt>
</dl>
</td>
<td width="60%">
Sets the user data associated with the window. This data is intended for use by the application that created the window. Its value is initially zero.

</td>
</tr>
<tr>
<td width="40%"><a id="GWLP_WNDPROC"></a><a id="gwlp_wndproc"></a><dl>
<dt><b>GWLP_WNDPROC</b></dt>
<dt>-4</dt>
</dl>
</td>
<td width="60%">
Sets a new address for the window procedure. 

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
<td width="40%"><a id="DWLP_DLGPROC"></a><a id="dwlp_dlgproc"></a><dl>
<dt><b>DWLP_DLGPROC</b></dt>
<dt>DWLP_MSGRESULT + sizeof(LRESULT)</dt>
</dl>
</td>
<td width="60%">
Sets the new pointer to the dialog box procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="DWLP_MSGRESULT"></a><a id="dwlp_msgresult"></a><dl>
<dt><b>DWLP_MSGRESULT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Sets the return value of a message processed in the dialog box procedure.

</td>
</tr>
<tr>
<td width="40%"><a id="DWLP_USER"></a><a id="dwlp_user"></a><dl>
<dt><b>DWLP_USER</b></dt>
<dt>DWLP_DLGPROC + sizeof(DLGPROC)</dt>
</dl>
</td>
<td width="60%">
Sets new extra information that is private to the application, such as handles or pointers.

</td>
</tr>
</table>
 


### -param dwNewLong [in]

Type: <b>LONG_PTR</b>

The replacement value. 


## -returns



Type: <strong>Type: <b>LONG_PTR</b>
</strong>

If the function succeeds, the return value is the previous value of the specified offset.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 

If the previous value is zero and the function succeeds, the return value is zero, but the function does not clear the last error information. To determine success or failure, clear the last error information by calling <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> with 0, then call <b>SetWindowLongPtr</b>. Function failure will be indicated by a return value of zero and a <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> result that is nonzero.




## -remarks



Certain window data is cached, so changes you make using <b>SetWindowLongPtr</b> will not take effect until you call the <a href="https://msdn.microsoft.com/e0a28590-0fed-4ffa-adcd-84b60df316b5">SetWindowPos</a> function.

If you use <b>SetWindowLongPtr</b> with the <b>GWLP_WNDPROC</b> index to replace the window procedure, the window procedure must conform to the guidelines specified in the description of the <a href="https://msdn.microsoft.com/4bb1cc3d-78db-4546-8ae9-d29fc6ee8f7c">WindowProc</a> callback function. 

If you use <b>SetWindowLongPtr</b> with the <b>DWLP_MSGRESULT</b> index to set the return value for a message processed by a dialog box procedure, the dialog box procedure should return <b>TRUE</b> directly afterward. Otherwise, if you call any function that results in your dialog box procedure receiving a window message, the nested window message could overwrite the return value you set by using <b>DWLP_MSGRESULT</b>. 

Calling <b>SetWindowLongPtr</b> with the <b>GWLP_WNDPROC</b> index creates a subclass of the window class used to create the window. An application can subclass a system class, but should not subclass a window class created by another process. The <b>SetWindowLongPtr</b> function creates the window subclass by changing the window procedure associated with a particular window class, causing the system to call the new window procedure instead of the previous one. An application must pass any messages not processed by the new window procedure to the previous window procedure by calling <a href="https://msdn.microsoft.com/667449cd-1eea-43de-8268-3da73022d7ac">CallWindowProc</a>. This allows the application to create a chain of window procedures. 

Reserve extra window memory by specifying a nonzero value in the 
				<b>cbWndExtra</b> member of the <a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a> structure used with the <a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a> function. 

Do not call <b>SetWindowLongPtr</b> with the <b>GWLP_HWNDPARENT</b> index to change the parent of a child window. Instead, use the <a href="https://msdn.microsoft.com/a13f1cfc-dedc-4190-826f-b29b731e76df">SetParent</a> function. 

If the window has a class style of <b>CS_CLASSDC</b> or <b>CS_PARENTDC</b>, do not set the extended window styles <b>WS_EX_COMPOSITED</b> or <b>WS_EX_LAYERED</b>.

 Calling <b>SetWindowLongPtr</b> to set the style on a progressbar will reset its position.




## -see-also




<a href="https://msdn.microsoft.com/667449cd-1eea-43de-8268-3da73022d7ac">CallWindowProc</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a48b63f7-b5b4-49fb-b201-78c3b27ac60a">GetWindowLongPtr</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/a13f1cfc-dedc-4190-826f-b29b731e76df">SetParent</a>



<a href="https://msdn.microsoft.com/f7e60154-b52c-4dee-b6dd-b6a4882ad4a9">WNDCLASSEX</a>



<a href="https://msdn.microsoft.com/6ef633db-af76-42d6-b211-96846578eaac">Window Classes</a>



<a href="https://msdn.microsoft.com/4bb1cc3d-78db-4546-8ae9-d29fc6ee8f7c">WindowProc</a>
 

 

