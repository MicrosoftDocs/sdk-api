---
UID: NF:winuser.ScrollWindow
title: ScrollWindow function (winuser.h)
author: windows-sdk-content
description: The ScrollWindow function scrolls the contents of the specified window's client area.
old-location: controls\ScrollWindow.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\scrollwindow.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ScrollWindow, ScrollWindow function [Windows Controls], _win32_ScrollWindow, _win32_ScrollWindow_cpp, controls.ScrollWindow, controls._win32_ScrollWindow, winuser/ScrollWindow
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
api_name:
 - ScrollWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ScrollWindow function


## -description


The <b>ScrollWindow</b> function scrolls the contents of the specified window's client area.  
<div class="alert"><b>Note</b>  The <b>ScrollWindow</b> function is provided for backward compatibility. New applications should use the <a href="https://msdn.microsoft.com/en-us/library/Bb787593(v=VS.85).aspx">ScrollWindowEx</a> function.</div><div> </div>

## -parameters




### -param hWnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the window where the client area is to be scrolled. 


### -param XAmount [in]

Type: <b>int</b>

Specifies the amount, in device units, of horizontal scrolling. If the window being scrolled has the <a href="https://msdn.microsoft.com/BE908D51-25DD-45d0-B6AA-28B4C627715B">CS_OWNDC</a> or <a href="https://msdn.microsoft.com/BE908D51-25DD-45d0-B6AA-28B4C627715B">CS_CLASSDC</a> style, then this parameter uses logical units rather than device units. This parameter must be a negative value to scroll the content of the window to the left. 


### -param YAmount [in]

Type: <b>int</b>

Specifies the amount, in device units, of vertical scrolling. If the window being scrolled has the <a href="https://msdn.microsoft.com/BE908D51-25DD-45d0-B6AA-28B4C627715B">CS_OWNDC</a> or <a href="https://msdn.microsoft.com/BE908D51-25DD-45d0-B6AA-28B4C627715B">CS_CLASSDC</a> style, then this parameter uses logical units rather than device units. This parameter must be a negative value to scroll the content of the window up. 


### -param lpRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure specifying the portion of the client area to be scrolled. If this parameter is <b>NULL</b>, the entire client area is scrolled. 


### -param lpClipRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to the 
					<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the coordinates of the clipping rectangle. Only device bits within the clipping rectangle are affected. Bits scrolled from the outside of the rectangle to the inside are painted; bits scrolled from the inside of the rectangle to the outside are not painted. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If the caret is in the window being scrolled, <b>ScrollWindow</b> automatically hides the caret to prevent it from being erased and then restores the caret after the scrolling is finished. The caret position is adjusted accordingly. 

The area uncovered by <b>ScrollWindow</b> is not repainted, but it is combined into the window's update region. The application eventually receives a <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message notifying it that the region must be repainted. To repaint the uncovered area at the same time the scrolling is in action, call the <a href="https://msdn.microsoft.com/51a50f1f-7b4d-4acd-83a0-1877f5181766">UpdateWindow</a> function immediately after calling <b>ScrollWindow</b>. 

If the 
				<i>lpRect</i> parameter is <b>NULL</b>, the positions of any child windows in the window are offset by the amount specified by the 
				<i>XAmount</i> and 
				<i>YAmount</i> parameters; invalid (unpainted) areas in the window are also offset. <b>ScrollWindow</b> is faster when 
				<i>lpRect</i> is <b>NULL</b>. 

If 
				<i>lpRect</i> is not <b>NULL</b>, the positions of child windows are not changed and invalid areas in the window are not offset. To prevent updating problems when 
				<i>lpRect</i> is not <b>NULL</b>, call 
				<a href="https://msdn.microsoft.com/51a50f1f-7b4d-4acd-83a0-1877f5181766">UpdateWindow</a> to repaint the window before calling <b>ScrollWindow</b>. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/Bb787531(v=VS.85).aspx">Scrolling Text with the WM_PAINT Message</a>.

<div class="code"></div>



## -see-also




<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787589(v=VS.85).aspx">ScrollDC</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787593(v=VS.85).aspx">ScrollWindowEx</a>



<a href="https://msdn.microsoft.com/51a50f1f-7b4d-4acd-83a0-1877f5181766">UpdateWindow</a>
 

 

