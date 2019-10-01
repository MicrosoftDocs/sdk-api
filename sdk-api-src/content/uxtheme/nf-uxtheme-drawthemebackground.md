---
UID: NF:uxtheme.DrawThemeBackground
title: DrawThemeBackground function (uxtheme.h)
author: windows-sdk-content
description: Draws the border and fill defined by the visual style for the specified control part.
old-location: controls\DrawThemeBackground.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemebackground.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawThemeBackground, DrawThemeBackground function [Windows Controls], controls.DrawThemeBackground, controls.inet_DrawThemeBackground, inet_DrawThemeBackground, inet_DrawThemeBackground_cpp, uxtheme/DrawThemeBackground
ms.topic: function
f1_keywords: 
 - "uxtheme/DrawThemeBackground"
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
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrawThemeBackground function


## -description


Draws the border and fill defined by the visual style for the specified control part.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HDC</a></b>

HDC used for drawing the theme-defined background image.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part to draw. See <a href="https://docs.microsoft.com/windows/desktop/Controls/parts-and-states">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part to draw. See <a href="https://docs.microsoft.com/windows/desktop/Controls/parts-and-states">Parts and States</a>.


### -param pRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the rectangle, in logical coordinates, in which the background image is drawn. 


### -param pClipRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains a clipping rectangle. This parameter may be set to <b>NULL</b>.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Drawing operations are scaled to fit and not exceed the rectangle specified in <i>pRect</i>. Your application should not draw outside the rectangle specified by <i>pClipRect</i>.


#### Examples

Prior to calling <b>DrawThemeBackground</b> to draw the background image for a window, you may call <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-isthemebackgroundpartiallytransparent">IsThemeBackgroundPartiallyTransparent</a>. This method determines whether <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-drawthemeparentbackground">DrawThemeParentBackground</a> should be called to draw in backgrounds behind partially-transparent or alpha-blended child controls, and is demonstrated in the following example.
		


```cpp
if (_hTheme)
{
  if (IsThemeBackgroundPartiallyTransparent(_hTheme, BP_PUSHBUTTON, _iStateId))
  {
    DrawThemeParentBackground(_hwnd, hdcPaint, prcPaint);
  }

  DrawThemeBackground(_hTheme,
                    hdcPaint,
                    BP_PUSHBUTTON,
                    _iStateId,
                    &rcClient,
                    prcPaint);
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/property-typedefs">Property Identifiers</a>
 

 

