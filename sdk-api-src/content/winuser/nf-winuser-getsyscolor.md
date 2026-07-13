---
UID: NF:winuser.GetSysColor
title: GetSysColor function (winuser.h)
description: Retrieves the current color of the specified display element.
helpviewer_keywords: ["COLOR_3DDKSHADOW","COLOR_3DFACE","COLOR_3DHIGHLIGHT","COLOR_3DHILIGHT","COLOR_3DLIGHT","COLOR_3DSHADOW","COLOR_ACTIVEBORDER","COLOR_ACTIVECAPTION","COLOR_APPWORKSPACE","COLOR_BACKGROUND","COLOR_BTNFACE","COLOR_BTNHIGHLIGHT","COLOR_BTNHILIGHT","COLOR_BTNSHADOW","COLOR_BTNTEXT","COLOR_CAPTIONTEXT","COLOR_DESKTOP","COLOR_GRADIENTACTIVECAPTION","COLOR_GRADIENTINACTIVECAPTION","COLOR_GRAYTEXT","COLOR_HIGHLIGHT","COLOR_HIGHLIGHTTEXT","COLOR_HOTLIGHT","COLOR_INACTIVEBORDER","COLOR_INACTIVECAPTION","COLOR_INACTIVECAPTIONTEXT","COLOR_INFOBK","COLOR_INFOTEXT","COLOR_MENU","COLOR_MENUBAR","COLOR_MENUHILIGHT","COLOR_MENUTEXT","COLOR_SCROLLBAR","COLOR_WINDOW","COLOR_WINDOWFRAME","COLOR_WINDOWTEXT","GetSysColor","GetSysColor function [Windows and Messages]","_win32_getsyscolor","base.getsyscolor","winmsg.getsyscolor","winui.getsyscolor","winuser/GetSysColor"]
old-location: winmsg\getsyscolor.htm
tech.root: winmsg
ms.assetid: 165c1781-161e-4ab2-98c9-eec4e9098d09
ms.date: 12/05/2018
ms.keywords: COLOR_3DDKSHADOW, COLOR_3DFACE, COLOR_3DHIGHLIGHT, COLOR_3DHILIGHT, COLOR_3DLIGHT, COLOR_3DSHADOW, COLOR_ACTIVEBORDER, COLOR_ACTIVECAPTION, COLOR_APPWORKSPACE, COLOR_BACKGROUND, COLOR_BTNFACE, COLOR_BTNHIGHLIGHT, COLOR_BTNHILIGHT, COLOR_BTNSHADOW, COLOR_BTNTEXT, COLOR_CAPTIONTEXT, COLOR_DESKTOP, COLOR_GRADIENTACTIVECAPTION, COLOR_GRADIENTINACTIVECAPTION, COLOR_GRAYTEXT, COLOR_HIGHLIGHT, COLOR_HIGHLIGHTTEXT, COLOR_HOTLIGHT, COLOR_INACTIVEBORDER, COLOR_INACTIVECAPTION, COLOR_INACTIVECAPTIONTEXT, COLOR_INFOBK, COLOR_INFOTEXT, COLOR_MENU, COLOR_MENUBAR, COLOR_MENUHILIGHT, COLOR_MENUTEXT, COLOR_SCROLLBAR, COLOR_WINDOW, COLOR_WINDOWFRAME, COLOR_WINDOWTEXT, GetSysColor, GetSysColor function [Windows and Messages], _win32_getsyscolor, base.getsyscolor, winmsg.getsyscolor, winui.getsyscolor, winuser/GetSysColor
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetSysColor
 - winuser/GetSysColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-RTCore-NTUser-syscolors-l1-1-0.dll
 - minuser.dll
 - api-ms-win-ntuser-ie-window-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-rtcore-ntuser-sysparams-l1-1-0.dll
 - Ext-MS-Win-NTUser-SysParaMS-Ext-L1-1-0.dll
api_name:
 - GetSysColor
---

# GetSysColor function


## -description

Retrieves the current color of the specified display element. Display elements are the parts of a window and the display that appear on the system display screen.

## -parameters

### -param nIndex [in]

Type: <b>int</b>

The display element whose color is to be retrieved. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COLOR_3DDKSHADOW"></a><a id="color_3ddkshadow"></a><dl>
<dt><b>COLOR_3DDKSHADOW</b></dt>
<dt>21</dt>
</dl>
</td>
<td width="60%">
Dark shadow for three-dimensional display elements.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_3DFACE"></a><a id="color_3dface"></a><dl>
<dt><b>COLOR_3DFACE</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
Face color for three-dimensional display elements and for dialog box backgrounds.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_3DHIGHLIGHT"></a><a id="color_3dhighlight"></a><dl>
<dt><b>COLOR_3DHIGHLIGHT</b></dt>
<dt>20</dt>
</dl>
</td>
<td width="60%">
Highlight color for three-dimensional display elements (for edges facing the light source.)

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_3DHILIGHT"></a><a id="color_3dhilight"></a><dl>
<dt><b>COLOR_3DHILIGHT</b></dt>
<dt>20</dt>
</dl>
</td>
<td width="60%">
Highlight color for three-dimensional display elements (for edges facing the light source.)

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_3DLIGHT"></a><a id="color_3dlight"></a><dl>
<dt><b>COLOR_3DLIGHT</b></dt>
<dt>22</dt>
</dl>
</td>
<td width="60%">
Light color for three-dimensional display elements (for edges facing the light source.)

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_3DSHADOW"></a><a id="color_3dshadow"></a><dl>
<dt><b>COLOR_3DSHADOW</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
Shadow color for three-dimensional display elements (for edges facing away from the light source).

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_ACTIVEBORDER"></a><a id="color_activeborder"></a><dl>
<dt><b>COLOR_ACTIVEBORDER</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Active window border.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_ACTIVECAPTION"></a><a id="color_activecaption"></a><dl>
<dt><b>COLOR_ACTIVECAPTION</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Active window title bar. 

The associated foreground color is <b>COLOR_CAPTIONTEXT</b>.

Specifies the left side color in the color gradient of an active window's title bar if the gradient effect is enabled.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_APPWORKSPACE"></a><a id="color_appworkspace"></a><dl>
<dt><b>COLOR_APPWORKSPACE</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
Background color of multiple document interface (MDI) applications.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_BACKGROUND"></a><a id="color_background"></a><dl>
<dt><b>COLOR_BACKGROUND</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Desktop.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_BTNFACE"></a><a id="color_btnface"></a><dl>
<dt><b>COLOR_BTNFACE</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
Face color for three-dimensional display elements and for dialog box backgrounds. The associated foreground color is <b>COLOR_BTNTEXT</b>.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="_COLOR_BTNHIGHLIGHT"></a><a id="_color_btnhighlight"></a><dl>
<dt><b>COLOR_BTNHIGHLIGHT</b></dt>
<dt>20</dt>
</dl>
</td>
<td width="60%">
Highlight color for three-dimensional display elements (for edges facing the light source.)

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="_COLOR_BTNHILIGHT"></a><a id="_color_btnhilight"></a><dl>
<dt><b>COLOR_BTNHILIGHT</b></dt>
<dt>20</dt>
</dl>
</td>
<td width="60%">
Highlight color for three-dimensional display elements (for edges facing the light source.)

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_BTNSHADOW"></a><a id="color_btnshadow"></a><dl>
<dt><b>COLOR_BTNSHADOW</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
Shadow color for three-dimensional display elements (for edges facing away from the light source).

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_BTNTEXT"></a><a id="color_btntext"></a><dl>
<dt><b>COLOR_BTNTEXT</b></dt>
<dt>18</dt>
</dl>
</td>
<td width="60%">
Text on push buttons. The associated background color is COLOR_BTNFACE.

</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_CAPTIONTEXT"></a><a id="color_captiontext"></a><dl>
<dt><b>COLOR_CAPTIONTEXT</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Text in caption, size box, and scroll bar arrow box. The associated background color is COLOR_ACTIVECAPTION.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_DESKTOP"></a><a id="color_desktop"></a><dl>
<dt><b>COLOR_DESKTOP</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Desktop.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_GRADIENTACTIVECAPTION"></a><a id="color_gradientactivecaption"></a><dl>
<dt><b>COLOR_GRADIENTACTIVECAPTION</b></dt>
<dt>27</dt>
</dl>
</td>
<td width="60%">
Right side color in the color gradient of an active window's title bar. COLOR_ACTIVECAPTION specifies the left side color. Use SPI_GETGRADIENTCAPTIONS with the 
<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a> function to determine whether the gradient effect is enabled.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_GRADIENTINACTIVECAPTION"></a><a id="color_gradientinactivecaption"></a><dl>
<dt><b>COLOR_GRADIENTINACTIVECAPTION</b></dt>
<dt>28</dt>
</dl>
</td>
<td width="60%">
Right side color in the color gradient of an inactive window's title bar. COLOR_INACTIVECAPTION specifies the left side color.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_GRAYTEXT"></a><a id="color_graytext"></a><dl>
<dt><b>COLOR_GRAYTEXT</b></dt>
<dt>17</dt>
</dl>
</td>
<td width="60%">
Grayed (disabled) text. This color is set to 0 if the current display driver does not support a solid gray color.

</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_HIGHLIGHT"></a><a id="color_highlight"></a><dl>
<dt><b>COLOR_HIGHLIGHT</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
Item(s) selected in a control. The associated foreground color is COLOR_HIGHLIGHTTEXT.

</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_HIGHLIGHTTEXT"></a><a id="color_highlighttext"></a><dl>
<dt><b>COLOR_HIGHLIGHTTEXT</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
Text of item(s) selected in a control. The associated background color is COLOR_HIGHLIGHT.

</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_HOTLIGHT"></a><a id="color_hotlight"></a><dl>
<dt><b>COLOR_HOTLIGHT</b></dt>
<dt>26</dt>
</dl>
</td>
<td width="60%">
Color for a hyperlink or hot-tracked item. The associated background color is COLOR_WINDOW.

</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_INACTIVEBORDER"></a><a id="color_inactiveborder"></a><dl>
<dt><b>COLOR_INACTIVEBORDER</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Inactive window border.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_INACTIVECAPTION"></a><a id="color_inactivecaption"></a><dl>
<dt><b>COLOR_INACTIVECAPTION</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Inactive window caption.

The associated foreground color is COLOR_INACTIVECAPTIONTEXT.

Specifies the left side color in the color gradient of an inactive window's title bar if the gradient effect is enabled. 

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_INACTIVECAPTIONTEXT"></a><a id="color_inactivecaptiontext"></a><dl>
<dt><b>COLOR_INACTIVECAPTIONTEXT</b></dt>
<dt>19</dt>
</dl>
</td>
<td width="60%">
Color of text in an inactive caption. The associated background color is COLOR_INACTIVECAPTION.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_INFOBK"></a><a id="color_infobk"></a><dl>
<dt><b>COLOR_INFOBK</b></dt>
<dt>24</dt>
</dl>
</td>
<td width="60%">
Background color for tooltip controls. The associated foreground color is COLOR_INFOTEXT.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_INFOTEXT"></a><a id="color_infotext"></a><dl>
<dt><b>COLOR_INFOTEXT</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
Text color for tooltip controls. The associated background color is COLOR_INFOBK.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_MENU"></a><a id="color_menu"></a><dl>
<dt><b>COLOR_MENU</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Menu background. The associated foreground color is COLOR_MENUTEXT.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_MENUHILIGHT"></a><a id="color_menuhilight"></a><dl>
<dt><b>COLOR_MENUHILIGHT</b></dt>
<dt>29</dt>
</dl>
</td>
<td width="60%">
The color used to highlight menu items when the menu appears as a flat menu (see 
<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>). The highlighted menu item is outlined with COLOR_HIGHLIGHT.

<b>Windows 2000, Windows 10 or greater:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_MENUBAR"></a><a id="color_menubar"></a><dl>
<dt><b>COLOR_MENUBAR</b></dt>
<dt>30</dt>
</dl>
</td>
<td width="60%">
The background color for the menu bar when menus appear as flat menus (see 
<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>). However, COLOR_MENU continues to specify the background color of the menu popup.

<b>Windows 2000, Windows 10 or greater:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_MENUTEXT"></a><a id="color_menutext"></a><dl>
<dt><b>COLOR_MENUTEXT</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Text in menus. The associated background color is COLOR_MENU.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_SCROLLBAR"></a><a id="color_scrollbar"></a><dl>
<dt><b>COLOR_SCROLLBAR</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Scroll bar gray area.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_WINDOW"></a><a id="color_window"></a><dl>
<dt><b>COLOR_WINDOW</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Window background. The associated foreground colors are COLOR_WINDOWTEXT and COLOR_HOTLITE.

</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_WINDOWFRAME"></a><a id="color_windowframe"></a><dl>
<dt><b>COLOR_WINDOWFRAME</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Window frame.

<b>Windows 10 or greater:</b> This value is not supported.
</td>
</tr>
<tr>
<td width="40%"><a id="COLOR_WINDOWTEXT"></a><a id="color_windowtext"></a><dl>
<dt><b>COLOR_WINDOWTEXT</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Text in windows. The associated background color is COLOR_WINDOW.

</td>
</tr>
</table>

## -returns

Type: <b>DWORD</b>

The function returns the red, green, blue (RGB) color value of the given element.

If the <i>nIndex</i> parameter is out of range, the return value is zero. Because zero is also a valid RGB value, you cannot use <b>GetSysColor</b> to determine whether a system color is supported by the current platform. Instead, use the <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush">GetSysColorBrush</a> function, which returns <b>NULL</b> if the color is not supported.

## -remarks

To display the component of the RGB  value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-getrvalue">GetRValue</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-getgvalue">GetGValue</a>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-getbvalue">GetBValue</a> macros.

System colors for monochrome displays are usually interpreted as shades of gray.

To paint with a system color brush, an application should use <code>GetSysColorBrush(nIndex)</code>, instead of <code>CreateSolidBrush(GetSysColor(nIndex))</code>, because <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush">GetSysColorBrush</a> returns a cached brush, instead of allocating a new one.

Color is an important visual element of most user interfaces. For guidelines about using color in your applications, see <a href="/windows/win32/uxguide/vis-color">Color - Win32</a> and <a href="/windows/apps/design/signature-experiences/color">Color in Windows 11</a>.

### Windows 10/11 system colors

This table shows the values that are supported in Windows 10 and Windows 11 with color values from the Windows 11 _Aquatic_ contrast theme.


| Color swatch | Description |
|---------|---------|
|:::image type="icon" source="images/sys-color/aquatic-color-window.png":::|  <b>COLOR_WINDOW</b></br>Background of pages, panes, popups, and windows.<br/><br/>Pair with COLOR_WINDOWTEXT       |
|:::image type="icon" source="images/sys-color/aquatic-color-windowtext.png"::: | <b>COLOR_WINDOWTEXT</b></br>Headings, body copy, lists, placeholder text, app and window borders, any UI that can't be interacted with.</br></br>Pair with COLOR_WINDOW        |
|:::image type="icon" source="images/sys-color/aquatic-color-hotlight.png":::| <b>COLOR_HOTLIGHT</b></br>Hyperlinks.</br></br>Pair with COLOR_WINDOW        |
|:::image type="icon" source="images/sys-color/aquatic-color-graytext.png":::|  <b>COLOR_GRAYTEXT</b></br>Inactive (disabled) UI.</br></br>Pair with COLOR_WINDOW       |
|:::image type="icon" source="images/sys-color/aquatic-color-highlighttext.png":::| <b>COLOR_HIGHLIGHTTEXT</b></br>Foreground color for text or UI that is in selected, interacted with (hover, pressed), or in progress.</br></br>Pair with COLOR_HIGHLIGHT        |
|:::image type="icon" source="images/sys-color/aquatic-color-highlight.png":::| <b>COLOR_HIGHLIGHT</b></br>Background or accent color for UI that is in selected, interacted with (hover, pressed), or in progress.</br></br>Pair with COLOR_HIGHLIGHTTEXT        |
|:::image type="icon" source="images/sys-color/aquatic-color-btntext.png":::| <b>COLOR_BTNTEXT</b></br>Foreground color for buttons and any UI that can be interacted with.</br></br>Pair with COLOR_3DFACE        |
|:::image type="icon" source="images/sys-color/aquatic-color-3dface.png":::| <b>COLOR_3DFACE</b></br>Background color for buttons and any UI that can be interacted with.</br></br>Pair with COLOR_BTNTEXT        |

These images show how the colors appear when used on a background set to **COLOR_WINDOW**.

| Example | Values |
|---------|---------|
|:::image type="content" source="images/sys-color/aquatic-example-windowtext.png" alt-text="A window with text using the window text color." border="false"::: | <b>COLOR_WINDOWTEXT</b> |
|:::image type="content" source="images/sys-color/aquatic-example-hotlight.png" alt-text="A window with hyperlink text using the hot light color." border="false":::| <b>COLOR_HOTLIGHT</b> |
|:::image type="content" source="images/sys-color/aquatic-example-graytext.png" alt-text="A window with inactive text using the gray text color." border="false":::| <b>COLOR_GRAYTEXT</b> |
|:::image type="content" source="images/sys-color/aquatic-example-highlighttext+highlight.png" alt-text="A window with text using the highlight text color on the highlight color." border="false":::|<b>COLOR_HIGHLIGHTTEXT + HIGHLIGHT</b> |
|:::image type="content" source="images/sys-color/aquatic-example-btntext+3dface.png" alt-text="A window with a button using the 3d face color and button text using the button text color." border="false":::| <b>COLOR_BTNTEXT + COLOR_3DFACE</b>

#### Examples

For an example, see 
<a href="/windows/desktop/api/winuser/nf-winuser-setsyscolors">SetSysColors</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush">CreateSolidBrush</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush">GetSysColorBrush</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setsyscolors">SetSysColors</a>



<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>