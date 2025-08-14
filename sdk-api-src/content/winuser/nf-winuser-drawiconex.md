---
UID: NF:winuser.DrawIconEx
title: DrawIconEx function (winuser.h)
description: Draws an icon or cursor into the specified device context, performing the specified raster operations, and stretching or compressing the icon or cursor as specified.
helpviewer_keywords: ["DI_COMPAT","DI_DEFAULTSIZE","DI_IMAGE","DI_MASK","DI_NOMIRROR","DI_NORMAL","DrawIconEx","DrawIconEx function [Menus and Other Resources]","_win32_DrawIconEx","_win32_drawiconex_cpp","menurc.drawiconex","winui._win32_drawiconex","winuser/DrawIconEx"]
old-location: menurc\drawiconex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\drawiconex.htm
ms.date: 12/05/2018
ms.keywords: DI_COMPAT, DI_DEFAULTSIZE, DI_IMAGE, DI_MASK, DI_NOMIRROR, DI_NORMAL, DrawIconEx, DrawIconEx function [Menus and Other Resources], _win32_DrawIconEx, _win32_drawiconex_cpp, menurc.drawiconex, winui._win32_drawiconex, winuser/DrawIconEx
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
 - DrawIconEx
 - winuser/DrawIconEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-gui-l1-1-1.dll
 - ext-ms-win-rtcore-ntuser-gui-l1-1-0.dll
 - ext-ms-win-ntuser-gui-l1-3-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - DrawIconEx
req.apiset: ext-ms-win-ntuser-gui-l1-1-0 (introduced in Windows 8)
---

# DrawIconEx function


## -description

Draws an icon or cursor into the specified device context, performing the specified raster operations, and stretching or compressing the icon or cursor as specified.

## -parameters

### -param hdc [in]

Type: <b>HDC</b>

A handle to the device context into which the icon or cursor will be drawn.

### -param xLeft [in]

Type: <b>int</b>

The logical x-coordinate of the upper-left corner of the icon or cursor.

### -param yTop [in]

Type: <b>int</b>

The logical y-coordinate of the upper-left corner of the icon or cursor.

### -param hIcon [in]

Type: <b>HICON</b>

A handle to the icon or cursor to be drawn. This parameter can identify an animated cursor.

### -param cxWidth [in]

Type: <b>int</b>

The logical width of the icon or cursor. If this parameter is zero and the <i>diFlags</i> parameter is <b>DI_DEFAULTSIZE</b>, the function uses the <b>SM_CXICON</b> system metric value to set the width. If this parameter is zero and <b>DI_DEFAULTSIZE</b> is not used, the function uses the actual resource width.

### -param cyWidth [in]

Type: <b>int</b>

The logical height of the icon or cursor. If this parameter is zero and the <i>diFlags</i> parameter is <b>DI_DEFAULTSIZE</b>, the function uses the <b>SM_CYICON</b> system metric value to set the width. If this parameter is zero and <b>DI_DEFAULTSIZE</b> is not used, the function uses the actual resource height.

### -param istepIfAniCur [in]

Type: <b>UINT</b>

The index of the frame to draw, if <i>hIcon</i> identifies an animated cursor. This parameter is ignored if <i>hIcon</i> does not identify an animated cursor.

### -param hbrFlickerFreeDraw [in, optional]

Type: <b>HBRUSH</b>

A handle to a brush that the system uses for flicker-free drawing. If <i>hbrFlickerFreeDraw</i> is a valid brush handle, the system creates an offscreen bitmap using the specified brush for the background color, draws the icon or cursor into the bitmap, and then copies the bitmap into the device context identified by <i>hdc</i>. If <i>hbrFlickerFreeDraw</i> is <b>NULL</b>, the system draws the icon or cursor directly into the device context.

### -param diFlags [in]

Type: <b>UINT</b>

The drawing flags. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DI_COMPAT"></a><a id="di_compat"></a><dl>
<dt><b>DI_COMPAT</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
 This flag is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="DI_DEFAULTSIZE"></a><a id="di_defaultsize"></a><dl>
<dt><b>DI_DEFAULTSIZE</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Draws the icon or cursor using the width and height specified by the system metric values for icons, if the <i>cxWidth</i> and <i>cyWidth</i> parameters are set to zero. If this flag is not specified and <i>cxWidth</i> and <i>cyWidth</i> are set to zero, the function uses the actual resource size. 

</td>
</tr>
<tr>
<td width="40%"><a id="DI_IMAGE"></a><a id="di_image"></a><dl>
<dt><b>DI_IMAGE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Draws the icon or cursor using the image. See Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="DI_MASK"></a><a id="di_mask"></a><dl>
<dt><b>DI_MASK</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Draws the icon or cursor using the mask. See Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="DI_NOMIRROR"></a><a id="di_nomirror"></a><dl>
<dt><b>DI_NOMIRROR</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Draws the icon as an unmirrored icon. By default, the icon is drawn as a mirrored icon if <i>hdc</i> is mirrored.

</td>
</tr>
<tr>
<td width="40%"><a id="DI_NORMAL"></a><a id="di_normal"></a><dl>
<dt><b>DI_NORMAL</b></dt>
<dt>0x0003</dt>
</dl>
</td>
<td width="60%">
Combination of <b>DI_IMAGE</b> and <b>DI_MASK</b>. See Remarks.

</td>
</tr>
</table>

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>DrawIconEx</b> function places the icon's upper-left corner at the location specified by the <i>xLeft</i> and <i>yTop</i> parameters. The location is subject to the current mapping mode of the device context.

If only one of the <b>DI_IMAGE</b> and <b>DI_MASK</b> flags is set, then the corresponding bitmap is drawn with the <b>SRCCOPY</b> <a href="/windows/win32/api/wingdi/nf-wingdi-bitblt">raster operation code</a>.

If both the <b>DI_IMAGE</b> and <b>DI_MASK</b> flags are set:
* If the icon or cursor is a 32-bit alpha-blended icon or cursor, then the image is drawn with <b>AC_SRC_OVER</b> <a href="/windows/win32/api/wingdi/ns-wingdi-blendfunction">blend function</a> and the mask is ignored.
* For all other icons or cursors, the mask is drawn with the <b>SRCAND</b> <a href="/windows/win32/api/wingdi/nf-wingdi-bitblt">raster operation code</a>, and the image is drawn with the <b>SRCINVERT</b> <a href="/windows/win32/api/wingdi/nf-wingdi-bitblt">raster operation code</a>

To duplicate <code>DrawIcon (hDC, X, Y, hIcon)</code>, call <b>DrawIconEx</b> as follows:

``` syntax
DrawIconEx (hDC, X, Y, hIcon, 0, 0, 0, NULL, DI_NORMAL | DI_COMPAT | DI_DEFAULTSIZE); 
```

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/nf-winuser-copyimage">CopyImage</a>

<a href="/windows/desktop/api/winuser/nf-winuser-drawicon">DrawIcon</a>

<a href="/windows/desktop/menurc/icons">Icons</a>

<a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a>

<b>Reference</b>

<a href="/windows/win32/api/wingdi/nf-wingdi-bitblt">BitBlt</a>

<a href="/windows/win32/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a>

<a href="/windows/win32/api/wingdi/ns-wingdi-blendfunction">BLENDFUNCTION</a>
