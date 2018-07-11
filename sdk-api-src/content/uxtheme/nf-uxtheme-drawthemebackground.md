---
UID: NF:uxtheme.DrawThemeBackground
title: DrawThemeBackground function
author: windows-sdk-content
description: Draws the border and fill defined by the visual style for the specified control part.
old-location: controls\DrawThemeBackground.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemebackground.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: DrawThemeBackground, DrawThemeBackground function [Windows Controls], controls.DrawThemeBackground, controls.inet_DrawThemeBackground, inet_DrawThemeBackground, inet_DrawThemeBackground_cpp, uxtheme/DrawThemeBackground
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uxtheme.h
req.include-header: 
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
req.typenames: BP_BUFFERFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
 - Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
 - xamlpalwp.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
 - DrawThemeBackground
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# DrawThemeBackground function


## -description


Draws the border and fill defined by the visual style for the specified control part.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/library/Bb759821(v=VS.85).aspx">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC used for drawing the theme-defined background image.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part to draw. See <a href="https://msdn.microsoft.com/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part to draw. See <a href="https://msdn.microsoft.com/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param pRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the rectangle, in logical coordinates, in which the background image is drawn. 


### -param pClipRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains a clipping rectangle. This parameter may be set to <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Drawing operations are scaled to fit and not exceed the rectangle specified in <i>pRect</i>. Your application should not draw outside the rectangle specified by <i>pClipRect</i>.


#### Examples


		Prior to calling <b>DrawThemeBackground</b> to draw the background image for a window, you may call <a href="https://msdn.microsoft.com/library/Bb759815(v=VS.85).aspx">IsThemeBackgroundPartiallyTransparent</a>. This method determines whether <a href="https://msdn.microsoft.com/library/Bb773306(v=VS.85).aspx">DrawThemeParentBackground</a> should be called to draw in backgrounds behind partially-transparent or alpha-blended child controls, and is demonstrated in the following example.
		

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if (_hTheme)
{
  if (IsThemeBackgroundPartiallyTransparent(_hTheme, BP_PUSHBUTTON, _iStateId))
  {
    DrawThemeParentBackground(_hwnd, hdcPaint, prcPaint);
  }

  DrawThemeBackground(_hTheme,
                    hdcPaint,
                    BP_PUSHBUTTON,
                    _iStateId,
                    &amp;rcClient,
                    prcPaint);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/Bb773213(v=VS.85).aspx">Property Identifiers</a>
 

 

