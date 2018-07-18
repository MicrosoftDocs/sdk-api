---
UID: NF:winuser.ScrollWindowEx
title: ScrollWindowEx function
author: windows-sdk-content
description: The ScrollWindowEx function scrolls the contents of the specified window's client area.
old-location: controls\ScrollWindowEx.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\scrollbars\scrollbarreference\scrollbarfunctions\scrollwindowex.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: SW_ERASE, SW_INVALIDATE, SW_SCROLLCHILDREN, SW_SMOOTHSCROLL, ScrollWindowEx, ScrollWindowEx function [Windows Controls], _win32_ScrollWindowEx, _win32_ScrollWindowEx_cpp, controls.ScrollWindowEx, controls._win32_ScrollWindowEx, winuser/ScrollWindowEx
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - ScrollWindowEx
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ScrollWindowEx function


## -description


The <b>ScrollWindowEx</b> function scrolls the contents of the specified window's client area. 


## -parameters




### -param hWnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the window where the client area is to be scrolled. 


### -param dx [in]

Type: <b>int</b>

Specifies the amount, in device units, of horizontal scrolling. This parameter must be a negative value to scroll to the left. 


### -param dy [in]

Type: <b>int</b>

Specifies the amount, in device units, of vertical scrolling. This parameter must be a negative value to scroll up. 


### -param prcScroll [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the portion of the client area to be scrolled. If this parameter is <b>NULL</b>, the entire client area is scrolled. 


### -param prcClip [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the coordinates of the clipping rectangle. Only device bits within the clipping rectangle are affected. Bits scrolled from the outside of the rectangle to the inside are painted; bits scrolled from the inside of the rectangle to the outside are not painted. This parameter may be <b>NULL</b>. 


### -param hrgnUpdate [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRGN</a></b>

Handle to the region that is modified to hold the region invalidated by scrolling. This parameter may be <b>NULL</b>. 


### -param prcUpdate [out]

Type: <b>LPRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that receives the boundaries of the rectangle invalidated by scrolling. This parameter may be <b>NULL</b>. 


### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies flags that control scrolling. This parameter can be a combination of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SW_ERASE"></a><a id="sw_erase"></a><dl>
<dt><b>SW_ERASE</b></dt>
</dl>
</td>
<td width="60%">
Erases the newly invalidated region by sending a 
						<a href="https://msdn.microsoft.com/3bdc37da-227c-4be1-bf0b-99704b8acbe1">WM_ERASEBKGND</a> message to the window when specified with the SW_INVALIDATE flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_INVALIDATE"></a><a id="sw_invalidate"></a><dl>
<dt><b>SW_INVALIDATE</b></dt>
</dl>
</td>
<td width="60%">
Invalidates the region identified by the 
						<i>hrgnUpdate</i> parameter after scrolling.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SCROLLCHILDREN"></a><a id="sw_scrollchildren"></a><dl>
<dt><b>SW_SCROLLCHILDREN</b></dt>
</dl>
</td>
<td width="60%">
Scrolls all child windows that intersect the rectangle pointed to by the 
						<i>prcScroll</i> parameter. The child windows are scrolled by the number of pixels specified by the 
						<i>dx</i> and 
						<i>dy</i> parameters. The system sends a 
						<a href="https://msdn.microsoft.com/552ddc26-fe63-449b-8c82-bb927a2c1c41">WM_MOVE</a> message to all child windows that intersect the 
						<i>prcScroll</i> rectangle, even if they do not move.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_SMOOTHSCROLL"></a><a id="sw_smoothscroll"></a><dl>
<dt><b>SW_SMOOTHSCROLL</b></dt>
</dl>
</td>
<td width="60%">

                Scrolls using smooth scrolling. Use the 
						<a href="https://msdn.microsoft.com/9f79d489-ff3f-437c-821e-fd353d712c7b">HIWORD</a> portion of the 
						<i>flags</i> parameter to indicate how much time, in milliseconds, the smooth-scrolling operation should take.

</td>
</tr>
</table>
 


## -returns



Type: <b>int</b>

If the function succeeds, the return value is SIMPLEREGION (rectangular invalidated region), COMPLEXREGION (nonrectangular invalidated region; overlapping rectangles), or NULLREGION (no invalidated region). 

If the function fails, the return value is ERROR. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the SW_INVALIDATE and SW_ERASE flags are not specified, <b>ScrollWindowEx</b> does not invalidate the area that is scrolled from. If either of these flags is set, <b>ScrollWindowEx</b> invalidates this area. The area is not updated until the application calls the <a href="https://msdn.microsoft.com/51a50f1f-7b4d-4acd-83a0-1877f5181766">UpdateWindow</a> function, calls the  <a href="https://msdn.microsoft.com/c6cb7f74-237e-4d3e-a852-894da36e990c">RedrawWindow</a> function (specifying the RDW_UPDATENOW or RDW_ERASENOW flag), or retrieves the 
				<a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message from the application queue. 

If the window has the <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">WS_CLIPCHILDREN</a> style, the returned areas specified by 
				<i>hrgnUpdate</i> and 
				<i>prcUpdate</i> represent the total area of the scrolled window that must be updated, including any areas in child windows that need updating. 

If the SW_SCROLLCHILDREN flag is specified, the system does not properly update the screen if part of a child window is scrolled. The part of the scrolled child window that lies outside the source rectangle is not erased and is not properly redrawn in its new destination. To move child windows that do not lie completely within the rectangle specified by 
				<i>prcScroll</i>, use the <a href="https://msdn.microsoft.com/2758de7b-c218-4a9b-b11b-b189301f7514">DeferWindowPos</a> function. The cursor is repositioned if the SW_SCROLLCHILDREN flag is set and the caret rectangle intersects the scroll rectangle. 

All input and output coordinates (for 
				<i>prcScroll</i>, 
				<i>prcClip</i>, 
				<i>prcUpdate</i>, and 
				<i>hrgnUpdate</i>) are determined as client coordinates, regardless of whether the window has the <a href="https://msdn.microsoft.com/BE908D51-25DD-45d0-B6AA-28B4C627715B">CS_OWNDC</a> or <a href="https://msdn.microsoft.com/BE908D51-25DD-45d0-B6AA-28B4C627715B">CS_CLASSDC</a> class style. Use the 
				<a href="https://msdn.microsoft.com/670a16fb-842e-4250-9ad7-dc08e849c2ba">LPtoDP</a> and 
				<a href="https://msdn.microsoft.com/0106867c-e8c5-4826-8cba-60c29e1d021a">DPtoLP</a> functions to convert to and from logical coordinates, if necessary. 


#### Examples

For an example, see <a href="Using_Scroll_Bars.htm">Scrolling Text with the WM_PAINT Message</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0106867c-e8c5-4826-8cba-60c29e1d021a">DPtoLP</a>



<a href="https://msdn.microsoft.com/2758de7b-c218-4a9b-b11b-b189301f7514">DeferWindowPos</a>



<a href="https://msdn.microsoft.com/670a16fb-842e-4250-9ad7-dc08e849c2ba">LPtoDP</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/c6cb7f74-237e-4d3e-a852-894da36e990c">RedrawWindow</a>



<a href="https://msdn.microsoft.com/51a50f1f-7b4d-4acd-83a0-1877f5181766">UpdateWindow</a>
 

 

