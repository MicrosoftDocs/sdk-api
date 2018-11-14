---
UID: NF:commctrl.DrawStatusTextA
title: DrawStatusTextA function
author: windows-sdk-content
description: The DrawStatusText function draws the specified text in the style of a status window with borders.
old-location: controls\DrawStatusText.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\status\functions\drawstatustext.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DrawStatusText, DrawStatusText function [Windows Controls], DrawStatusTextA, DrawStatusTextW, SBT_NOBORDERS, SBT_POPOUT, SBT_RTLREADING, _win32_DrawStatusText, _win32_DrawStatusText_cpp, commctrl/DrawStatusText, commctrl/DrawStatusTextA, commctrl/DrawStatusTextW, controls.DrawStatusText, controls._win32_DrawStatusText
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DrawStatusTextW (Unicode) and DrawStatusTextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DrawStatusText
 - DrawStatusTextA
 - DrawStatusTextW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DrawStatusTextA
: 
---

# DrawStatusTextA function


## -description


The <b>DrawStatusText</b> function draws the specified text in the style of a status window with borders.


## -parameters




### -param hDC

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HDC</a></b>

Handle to the display context for the window. 


### -param lprc

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the position, in client coordinates, of the rectangle in which the text is drawn. The function draws the borders just inside the edges of the specified rectangle. 


### -param pszText

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCTSTR</a></b>

Pointer to a null-terminated string that specifies the text to display. Tab characters in the string determine whether the string is left-aligned, right-aligned, or centered. 


### -param uFlags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Text drawing flags. This parameter can be a combination of these values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SBT_NOBORDERS"></a><a id="sbt_noborders"></a><dl>
<dt><b>SBT_NOBORDERS</b></dt>
</dl>
</td>
<td width="60%">
Prevents borders from being drawn around the specified text.

</td>
</tr>
<tr>
<td width="40%"><a id="SBT_POPOUT"></a><a id="sbt_popout"></a><dl>
<dt><b>SBT_POPOUT</b></dt>
</dl>
</td>
<td width="60%">
Draws highlighted borders that make the text stand out.

</td>
</tr>
<tr>
<td width="40%"><a id="SBT_RTLREADING"></a><a id="sbt_rtlreading"></a><dl>
<dt><b>SBT_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the string pointed to by 
						<i>pszText</i> will be displayed in the opposite direction to the text in the parent window. 

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



Normal windows display text left-to-right (LTR). Windows can be <i>mirrored</i> to display languages such as Hebrew or Arabic that read right-to-left (RTL). Normally, the <i>pszText</i> string will be displayed in the same direction as the text in its parent window. If SBT_RTLREADING is set, the <i>pszText</i> string will read in the opposite direction from the text in the parent window.



