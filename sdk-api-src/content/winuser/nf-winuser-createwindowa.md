---
UID: NF:winuser.CreateWindowA
title: CreateWindowA macro
author: windows-sdk-content
description: Creates an overlapped, pop-up, or child window.
old-location: winmsg\createwindow.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\createwindow.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateWindow, CreateWindow function [Windows and Messages], CreateWindowA, CreateWindowW, _win32_CreateWindow, _win32_createwindow_cpp, winmsg.createwindow, winui._win32_createwindow, winuser/CreateWindow, winuser/CreateWindowA, winuser/CreateWindowW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateWindowW (Unicode) and CreateWindowA (ANSI)
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
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - CreateWindow
 - CreateWindowA
 - CreateWindowW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CreateWindowA macro


## -description


Creates an overlapped, pop-up, or child window. It specifies the window class, window title, window style, and (optionally) the initial position and size of the window. The function also specifies the window's parent or owner, if any, and the window's menu.

To use extended window styles in addition to the styles supported by <b>CreateWindow</b>, use the <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function.


## -parameters




### -param lpClassName [in, optional]

Type: <b>LPCTSTR</b>

A <b>null</b>-terminated string or a class atom created by a previous call to the <a href="https://msdn.microsoft.com/485115e5-b4ec-4e93-89ce-eee229ccabb7">RegisterClass</a> or <a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a> function. The atom must be in the low-order word of <i>lpClassName</i>; the high-order word must be zero. If <i>lpClassName</i> is a string, it specifies the window class name. The class name can be any name registered with <b>RegisterClass</b> or <b>RegisterClassEx</b>, provided that the module that registers the class is also the module that creates the window. The class name can also be any of the predefined system class names. For a list of system class names, see the Remarks section. 


### -param lpWindowName [in, optional]

Type: <b>LPCTSTR</b>

The window name. If the window style specifies a title bar, the window title pointed to by <i>lpWindowName</i> is displayed in the title bar. When using <b>CreateWindow</b> to create controls, such as buttons, check boxes, and static controls, use <i>lpWindowName</i> to specify the text of the control. When creating a static control with the <b>SS_ICON</b> style, use <i>lpWindowName</i> to specify the icon name or identifier. To specify an identifier, use the syntax "#<i>num</i>". 


### -param dwStyle [in]

Type: <b>DWORD</b>

The style of the window being created. This parameter can be a combination of the <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">window style values</a>, plus the control styles indicated in the Remarks section. 


### -param x [in]

Type: <b>int</b>

The initial horizontal position of the window. For an overlapped or pop-up window, the <i>x</i> parameter is the initial x-coordinate of the window's upper-left corner, in screen coordinates. For a child window, <i>x</i> is the x-coordinate of the upper-left corner of the window relative to the upper-left corner of the parent window's client area. If this parameter is set to <b>CW_USEDEFAULT</b>, the system selects the default position for the window's upper-left corner and ignores the <i>y</i> parameter. <b>CW_USEDEFAULT</b> is valid only for overlapped windows; if it is specified for a pop-up or child window, the <i>x</i> and <i>y</i> parameters are set to zero. 


### -param y [in]

Type: <b>int</b>

The initial vertical position of the window. For an overlapped or pop-up window, the <i>y</i> parameter is the initial y-coordinate of the window's upper-left corner, in screen coordinates. For a child window, <i>y</i> is the initial y-coordinate of the upper-left corner of the child window relative to the upper-left corner of the parent window's client area. For a list box, <i>y</i> is the initial y-coordinate of the upper-left corner of the list box's client area relative to the upper-left corner of the parent window's client area.

If an overlapped window is created with the <b>WS_VISIBLE</b> style bit set and the <i>x</i> parameter is set to <b>CW_USEDEFAULT</b>, then the <i>y</i> parameter determines how the window is shown. If the <i>y</i> parameter is <b>CW_USEDEFAULT</b>, then the window manager calls <a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a> with the <b>SW_SHOW</b> flag after the window has been created. If the <i>y</i> parameter is some other value, then the window manager calls <b>ShowWindow</b> with that value as the <i>nCmdShow</i> parameter.


### -param nWidth [in]

Type: <b>int</b>

The width, in device units, of the window. For overlapped windows, <i>nWidth</i> is either the window's width, in screen coordinates, or <b>CW_USEDEFAULT</b>. If <i>nWidth</i> is <b>CW_USEDEFAULT</b>, the system selects a default width and height for the window; the default width extends from the initial x-coordinate to the right edge of the screen, and the default height extends from the initial y-coordinate to the top of the icon area. <b>CW_USEDEFAULT</b> is valid only for overlapped windows; if <b>CW_USEDEFAULT</b> is specified for a pop-up or child window, <i>nWidth</i> and <i>nHeight</i> are set to zero. 


### -param nHeight [in]

Type: <b>int</b>

The height, in device units, of the window. For overlapped windows, <i>nHeight</i> is the window's height, in screen coordinates. If <i>nWidth</i> is set to <b>CW_USEDEFAULT</b>, the system ignores <i>nHeight</i>. 


### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the parent or owner window of the window being created. To create a child window or an owned window, supply a valid window handle. This parameter is optional for pop-up windows.
					

To create a <a href="window_features.htm">message-only window</a>, supply <b>HWND_MESSAGE</b> or a handle to an existing message-only window. 


### -param hMenu [in, optional]

Type: <b>HMENU</b>

A handle to a menu, or specifies a child-window identifier depending on the window style. For an overlapped or pop-up window, <i>hMenu</i> identifies the menu to be used with the window; it can be <b>NULL</b> if the class menu is to be used. For a child window, <i>hMenu</i> specifies the child-window identifier, an integer value used by a dialog box control to notify its parent about events. The application determines the child-window identifier; it must be unique for all child windows with the same parent window. 


### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the instance of the module to be associated with the window.


### -param lpParam [in, optional]

Type: <b>LPVOID</b>

A pointer to a value to be passed to the window through the <a href="https://msdn.microsoft.com/2d67fed4-43de-4151-b124-b710ea64e8a6">CREATESTRUCT</a> structure (<b>lpCreateParams</b> member) pointed to by the <i>lParam</i> param of the <a href="https://msdn.microsoft.com/d484d0fc-bad0-4fcb-bf4b-37cbc50846ee">WM_CREATE</a> message.  This message is sent to the created window by this function before it returns.

If an application calls <b>CreateWindow</b> to create a MDI client window, <i>lpParam</i> should point to a <a href="https://msdn.microsoft.com/795396d0-4d3b-4e55-b339-cf02cdfd9b46">CLIENTCREATESTRUCT</a> structure. If an MDI client window calls <b>CreateWindow</b> to create an MDI child window, <i>lpParam</i> should point to a <a href="https://msdn.microsoft.com/aac21a17-4302-4174-9d72-15366d964094">MDICREATESTRUCT</a> structure. <i>lpParam</i> may be <b>NULL</b> if no additional data is needed.


## -remarks



Before returning, <b>CreateWindow</b> sends a <a href="https://msdn.microsoft.com/d484d0fc-bad0-4fcb-bf4b-37cbc50846ee">WM_CREATE</a> message to the window procedure. For overlapped, pop-up, and child windows, <b>CreateWindow</b> sends <b>WM_CREATE</b>, <a href="https://msdn.microsoft.com/af2295e0-2d0b-4ac0-b689-16138022f4b7">WM_GETMINMAXINFO</a>, and <a href="https://msdn.microsoft.com/5dd0eda3-83a6-4077-a7a3-e371c9413b0f">WM_NCCREATE</a> messages to the window. The
 <i>lParam</i> parameter of the <b>WM_CREATE</b> message contains a pointer to a <a href="https://msdn.microsoft.com/2d67fed4-43de-4151-b124-b710ea64e8a6">CREATESTRUCT</a> structure. If the <b>WS_VISIBLE</b> style is specified, <b>CreateWindow</b> sends the window all the messages required to activate and show the window. 

If the created window is a child window, its default position is at the bottom of the Z-order. If the created window is a top-level window, its default position is at the top of the Z-order (but beneath all topmost windows unless the created window is itself topmost).

For information on controlling whether the Taskbar displays a button for the created window, see <a href="_win32_Taskbar">Managing Taskbar Buttons</a>. 

For information on removing a window, see the <a href="https://msdn.microsoft.com/054fa847-7d6e-4c73-bf8c-b75203713b3e">DestroyWindow</a> function.

The following predefined system classes can be specified in the <i>lpClassName</i> parameter. Note the corresponding control styles you can use in the <i>dwStyle</i> parameter.

				

<table class="clsStd">
<tr>
<th>System class</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>BUTTON</b></td>
<td>
Designates a small rectangular child window that represents a button the user can click to turn it on or off. Button controls can be used alone or in groups, and they can either be labeled or appear without text. Button controls typically change appearance when the user clicks them. For more information, see <a href="_win32_Buttons">Buttons</a>


For a table of the button styles you can specify in the <i>dwStyle</i> parameter, see <a href="_win32_Button_Styles">Button Styles</a>.

</td>
</tr>
<tr>
<td><b>COMBOBOX</b></td>
<td>
Designates a control consisting of a list box and a selection field similar to an edit control. When using this style, an application should either display the list box at all times or enable a drop-down list box. If the list box is visible, typing characters into the selection field highlights the first list box entry that matches the characters typed. Conversely, selecting an item in the list box displays the selected text in the selection field. 

For more information, see <a href="_win32_Combo_Boxes">Combo Boxes</a>. For a table of the combo box styles you can specify in the <i>dwStyle</i> parameter, see <a href="_win32_Combo_Box_Styles">Combo Box Styles</a>.

</td>
</tr>
<tr>
<td><b>EDIT</b></td>
<td>
Designates a rectangular child window into which the user can type text from the keyboard. The user selects the control and gives it the keyboard focus by clicking it or moving to it by pressing the TAB key. The user can type text when the edit control displays a flashing caret; use the mouse to move the cursor, select characters to be replaced, or position the cursor for inserting characters; or use the BACKSPACE key to delete characters. For more information, see <a href="_win32_Edit_Controls">Edit Controls</a>.

For a table of the edit control styles you can specify in the <i>dwStyle</i> parameter, see <a href="_win32_Edit_Control_Styles">Edit Control Styles</a>.

</td>
</tr>
<tr>
<td><b>LISTBOX</b></td>
<td>
Designates a list of character strings. Specify this control whenever an application must present a list of names, such as file names, from which the user can choose. The user can select a string by clicking it. A selected string is highlighted, and a notification message is passed to the parent window. For more information, see <a href="_win32_List_Boxes">List Boxes</a>.

For a table of the list box styles you can specify in the <i>dwStyle</i> parameter, see <a href="_win32_List_Box_Styles">List Box Styles</a>.

</td>
</tr>
<tr>
<td><b>MDICLIENT</b></td>
<td>
Designates an MDI client window. This window receives messages that control the MDI application's child windows. The recommended style bits are <b>WS_CLIPCHILDREN</b> and <b>WS_CHILD</b>. Specify the <b>WS_HSCROLL</b> and <b>WS_VSCROLL</b> styles to create an MDI client window that allows the user to scroll MDI child windows into view.

 For more information, see <a href="https://msdn.microsoft.com/beb41067-91ed-4f63-af8f-1000ba82a3b1">Multiple Document Interface</a>.

</td>
</tr>
<tr>
<td><b>RichEdit</b></td>
<td>
Designates a Microsoft Rich Edit 1.0 control. This window lets the user view and edit text with character and paragraph formatting, and can include embedded Component Object Model (COM) objects. For more information, see <a href="_win32_Rich_Edit_Controls">Rich Edit Controls</a>.

For a table of the rich edit control styles you can specify in the <i>dwStyle</i> parameter, see <a href="_win32_Rich_Edit_Control_Styles">Rich Edit Control Styles</a>.

</td>
</tr>
<tr>
<td><b>RICHEDIT_CLASS</b></td>
<td>
Designates a Microsoft Rich Edit 2.0 control. This controls let the user view and edit text with character and paragraph formatting, and can include embedded COM objects. For more information, see <a href="_win32_Rich_Edit_Controls">Rich Edit Controls</a>.

For a table of the rich edit control styles you can specify in the <i>dwStyle</i> parameter, see <a href="_win32_Rich_Edit_Control_Styles">Rich Edit Control Styles</a>.

</td>
</tr>
<tr>
<td><b>SCROLLBAR</b></td>
<td>
Designates a rectangle that contains a scroll box and has direction arrows at both ends. The scroll bar sends a notification message to its parent window whenever the user clicks the control. The parent window is responsible for updating the position of the scroll box, if necessary. For more information, see <a href="_win32_Scroll_Bars">Scroll Bars</a>.

For a table of the scroll bar control styles you can specify in the <i>dwStyle</i> parameter, see <a href="_win32_Scroll_Bar_Control_Styles">Scroll Bar Control Styles</a>.

</td>
</tr>
<tr>
<td><b>STATIC</b></td>
<td>
Designates a simple text field, box, or rectangle used to label, box, or separate other controls. Static controls take no input and provide no output. For more information, see <a href="_win32_Static_Controls">Static Controls</a>.

For a table of the static control styles you can specify in the <i>dwStyle</i> parameter, see <a href="_win32_Static_Control_Styles">Static Control Styles</a>.

</td>
</tr>
</table>
 

<b>CreateWindow</b> is implemented as a call to the <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function, as shown below.

<pre class="syntax" xml:space="preserve"><code>#define CreateWindowA(lpClassName, lpWindowName, dwStyle, x, y, nWidth, nHeight, hWndParent, hMenu, hInstance, lpParam)\
CreateWindowExA(0L, lpClassName, lpWindowName, dwStyle, x, y, nWidth, nHeight, hWndParent, hMenu, hInstance, lpParam)

#define CreateWindowW(lpClassName, lpWindowName, dwStyle, x, y, nWidth, nHeight, hWndParent, hMenu, hInstance, lpParam)\
CreateWindowExW(0L, lpClassName, lpWindowName, dwStyle, x, y, nWidth, nHeight, hWndParent, hMenu, hInstance, lpParam)

#ifdef UNICODE
#define CreateWindow  CreateWindowW
#else
#define CreateWindow  CreateWindowA
#endif</code></pre>

#### Examples

For an example, see <a href="https://msdn.microsoft.com/ea9e36c9-b10d-441e-b1b5-1ab93e009e1d">Using Window Classes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/35dff281-3b11-4954-85cf-a0f1c9ed346a">About the Multiple Document Interface</a>



<a href="http://msdn.microsoft.com/en-us/library/bb775491%28v=VS.85%29.aspx ">Common Control Window Classes</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/054fa847-7d6e-4c73-bf8c-b75203713b3e">DestroyWindow</a>



<a href="https://msdn.microsoft.com/6913efcd-4d12-4396-a4ae-f1fd6335f7a8">EnableWindow</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/485115e5-b4ec-4e93-89ce-eee229ccabb7">RegisterClass</a>



<a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/13ffef63-3e29-4ca7-a14d-48ff901d82b5">ShowWindow</a>



<a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a>



<a href="https://msdn.microsoft.com/d484d0fc-bad0-4fcb-bf4b-37cbc50846ee">WM_CREATE</a>



<a href="https://msdn.microsoft.com/af2295e0-2d0b-4ac0-b689-16138022f4b7">WM_GETMINMAXINFO</a>



<a href="https://msdn.microsoft.com/5dd0eda3-83a6-4077-a7a3-e371c9413b0f">WM_NCCREATE</a>



<a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

