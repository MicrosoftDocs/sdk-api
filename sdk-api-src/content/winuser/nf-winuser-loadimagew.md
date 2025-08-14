---
UID: NF:winuser.LoadImageW
title: LoadImageW function (winuser.h)
description: Loads an icon, cursor, animated cursor, or bitmap. (Unicode)
helpviewer_keywords: ["IMAGE_BITMAP", "IMAGE_CURSOR", "IMAGE_ICON", "LR_CREATEDIBSECTION", "LR_DEFAULTCOLOR", "LR_DEFAULTSIZE", "LR_LOADFROMFILE", "LR_LOADMAP3DCOLORS", "LR_LOADTRANSPARENT", "LR_MONOCHROME", "LR_SHARED", "LR_VGACOLOR", "LoadImage", "LoadImage function [Menus and Other Resources]", "LoadImageW", "_win32_LoadImage", "_win32_loadimage_cpp", "menurc.loadimage", "winui._win32_loadimage", "winuser/LoadImage", "winuser/LoadImageW"]
old-location: menurc\loadimage.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\loadimage.htm
ms.date: 12/05/2018
ms.keywords: IMAGE_BITMAP, IMAGE_CURSOR, IMAGE_ICON, LR_CREATEDIBSECTION, LR_DEFAULTCOLOR, LR_DEFAULTSIZE, LR_LOADFROMFILE, LR_LOADMAP3DCOLORS, LR_LOADTRANSPARENT, LR_MONOCHROME, LR_SHARED, LR_VGACOLOR, LoadImage, LoadImage function [Menus and Other Resources], LoadImageA, LoadImageW, _win32_LoadImage, _win32_loadimage_cpp, menurc.loadimage, winui._win32_loadimage, winuser/LoadImage, winuser/LoadImageA, winuser/LoadImageW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadImageW (Unicode) and LoadImageA (ANSI)
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
 - LoadImageW
 - winuser/LoadImageW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
 - LoadImage
 - LoadImageA
 - LoadImageW
req.apiset: ext-ms-win-ntuser-gui-l1-1-0 (introduced in Windows 8)
---

# LoadImageW function


## -description

Loads an icon, cursor, animated cursor, or bitmap.

## -parameters

### -param hInst [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module of either a DLL or executable (.exe) that contains the image to be loaded. For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>. Note that as of  32-bit Windows, an instance handle (<b>HINSTANCE</b>), such as the application instance handle exposed by system function call of <a href="/windows/desktop/api/winbase/nf-winbase-winmain">WinMain</a>, and a module handle (<b>HMODULE</b>) are the same thing.

To load a predefined image or a standalone resource (icon, cursor, or bitmap file), set this parameter to <b>NULL</b>.

### -param name [in]

Type: <b>LPCTSTR</b>

The image to be loaded.

If the <i>hInst</i> parameter is non-<b>NULL</b> and the <i>fuLoad</i> parameter omits <b>LR_LOADFROMFILE</b>, <i>name</i> specifies the image resource in the <i>hInst</i> module.

If the image resource is to be loaded by name from the module, the <i>name</i> parameter is a pointer to a null-terminated string that contains the name of the image resource.

If the image resource is to be loaded by ordinal from the module, use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcew">MAKEINTRESOURCE</a> macro to convert the image ordinal into a form that can be passed to the <b>LoadImage</b> function.

If the <i>hInst</i> parameter is <b>NULL</b> and the <i>fuLoad</i> parameter omits the <b>LR_LOADFROMFILE</b> value and includes the <b>LR_SHARED</b>, the <i>name</i> specifies the predefined image to load.

The predefined image identifiers are defined in `Winuser.h` and have the following prefixes:

| Prefix | Meaning |
|---|---|
| **OBM\_** | OEM bitmaps. Use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcew">MAKEINTRESOURCE</a> macro to pass these. |
| **OIC\_** | OEM icons. Use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcew">MAKEINTRESOURCE</a> macro to pass these. |
| **OCR\_** | OEM cursors. Use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcew">MAKEINTRESOURCE</a> macro to pass these. |
| **IDI\_** | [Standard icons](/windows/win32/menurc/about-icons) |
| **IDC\_** | [Standard cursors](/windows/win32/menurc/about-cursors) |

To pass OEM image identifiers constants to the <b>LoadImage</b> function, use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. For example, to load the <b>OCR_NORMAL</b> cursor, pass <code>MAKEINTRESOURCE(OCR_NORMAL)</code> as the <i>name</i> parameter, <b>NULL</b> as the <i>hInst</i> parameter, and <b>LR_SHARED</b> as one of the flags to the <i>fuLoad</i> parameter.

If the <i>hInst</i> parameter is <b>NULL</b> and the <i>fuLoad</i> parameter includes the <b>LR_LOADFROMFILE</b> value, <i>name</i> is the name of the file that contains the standalone resource (icon, cursor, or bitmap file), - for example, `c:\myicon.ico`.

For more information, see the Remarks section below.

### -param type [in]

Type: <b>UINT</b>

The type of image to be loaded.

This parameter can be one of the following values:

| Value | Meaning |
|---|---|
| **IMAGE\_BITMAP** | Loads a bitmap. |
| **IMAGE\_CURSOR** | Loads a cursor. |
| **IMAGE\_ICON** | Loads an icon. |

### -param cx [in]

Type: <b>int</b>

The width, in pixels, of the icon or cursor. If this parameter is zero and the <i>fuLoad</i> parameter is <b>LR_DEFAULTSIZE</b>, the function uses the <b>SM_CXICON</b> or <b>SM_CXCURSOR</b> system metric value to set the width. If this parameter is zero and <b>LR_DEFAULTSIZE</b> is not used, the function uses the actual resource width.

### -param cy [in]

Type: <b>int</b>

The height, in pixels, of the icon or cursor. If this parameter is zero and the <i>fuLoad</i> parameter is <b>LR_DEFAULTSIZE</b>, the function uses the <b>SM_CYICON</b> or <b>SM_CYCURSOR</b> system metric value to set the height. If this parameter is zero and <b>LR_DEFAULTSIZE</b> is not used, the function uses the actual resource height.

### -param fuLoad [in]

Type: <b>UINT</b>

This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LR_CREATEDIBSECTION"></a><a id="lr_createdibsection"></a><dl>
<dt><b>LR_CREATEDIBSECTION</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
When the <i>uType</i> parameter specifies <b>IMAGE_BITMAP</b>, causes the function to return a DIB section bitmap rather than a compatible bitmap. This flag is useful for loading a bitmap without mapping it to the colors of the display device.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_DEFAULTCOLOR"></a><a id="lr_defaultcolor"></a><dl>
<dt><b>LR_DEFAULTCOLOR</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The default flag; it does nothing. All it means is "not <b>LR_MONOCHROME</b>".

</td>
</tr>
<tr>
<td width="40%"><a id="LR_DEFAULTSIZE"></a><a id="lr_defaultsize"></a><dl>
<dt><b>LR_DEFAULTSIZE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Uses the width or height specified by the system metric values for cursors or icons, if the <i>cxDesired</i> or <i>cyDesired</i> values are set to zero. If this flag is not specified and <i>cxDesired</i> and <i>cyDesired</i> are set to zero, the function uses the actual resource size. If the resource contains multiple images, the function uses the size of the first image.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_LOADFROMFILE"></a><a id="lr_loadfromfile"></a><dl>
<dt><b>LR_LOADFROMFILE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Loads the standalone image from the file specified by  <i>name</i> (icon, cursor, or bitmap file).

</td>
</tr>
<tr>
<td width="40%"><a id="LR_LOADMAP3DCOLORS"></a><a id="lr_loadmap3dcolors"></a><dl>
<dt><b>LR_LOADMAP3DCOLORS</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Searches the color table for the image and replaces the following shades of gray with the corresponding 3-D color.
						
                        

<ul>
<li>Dk Gray, RGB(128,128,128) with <b>COLOR_3DSHADOW</b></li>
<li>Gray, RGB(192,192,192) with <b>COLOR_3DFACE</b></li>
<li>Lt Gray, RGB(223,223,223) with <b>COLOR_3DLIGHT</b></li>
</ul>
Do not use this option if you are loading a bitmap with a color depth greater than 8bpp.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_LOADTRANSPARENT"></a><a id="lr_loadtransparent"></a><dl>
<dt><b>LR_LOADTRANSPARENT</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Retrieves the color value of the first pixel in the image and replaces the corresponding entry in the color table with the default window color (<b>COLOR_WINDOW</b>). All pixels in the image that use that entry become the default window color. This value applies only to images that have corresponding color tables.

Do not use this option if you are loading a bitmap with a color depth greater than 8bpp.

If <i>fuLoad</i> includes both the <b>LR_LOADTRANSPARENT</b> and <b>LR_LOADMAP3DCOLORS</b> values, <b>LR_LOADTRANSPARENT</b> takes precedence. However, the color table entry is replaced with <b>COLOR_3DFACE</b> rather than <b>COLOR_WINDOW</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_MONOCHROME"></a><a id="lr_monochrome"></a><dl>
<dt><b>LR_MONOCHROME</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Loads the image in black and white.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_SHARED"></a><a id="lr_shared"></a><dl>
<dt><b>LR_SHARED</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Shares the image handle if the image is loaded multiple times. If <b>LR_SHARED</b> is not set, a second call to <b>LoadImage</b> for the same resource will load the image again and return a different handle. 

When you use this flag, the system will destroy the resource when it is no longer needed.

Do not use <b>LR_SHARED</b> for images that have non-standard sizes, that may change after loading, or that are loaded from a file.

When loading a system icon or cursor, you must use <b>LR_SHARED</b> or the function will fail to load the resource.

This function finds the first image in the cache with the requested resource name, regardless of the size requested.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_VGACOLOR"></a><a id="lr_vgacolor"></a><dl>
<dt><b>LR_VGACOLOR</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Uses true VGA colors.

</td>
</tr>
</table>

## -returns

Type: <b>HANDLE</b>

If the function succeeds, the return value is the handle of the newly loaded image.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <a href="/windows/desktop/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a>(<i>name</i>) is <b>TRUE</b>, then <i>name</i> specifies the integer identifier of the given resource. Otherwise, it is a pointer to a null-terminated string.

If the first character of the string is a pound sign (#), then the remaining characters represent a decimal number that specifies the integer identifier of the resource. For example, the string "#258" represents the identifier 258.

When you are finished using a bitmap, cursor, or icon you loaded without specifying the <b>LR_SHARED</b> flag, you can release its associated memory by calling one of the functions in the following table.

                


<table class="clsStd">
<tr>
<th>Resource</th>
<th>Release function</th>
</tr>
<tr>
<td>Bitmap</td>
<td>
<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>
</td>
</tr>
<tr>
<td>Cursor</td>
<td>
<a href="/windows/desktop/api/winuser/nf-winuser-destroycursor">DestroyCursor</a>
</td>
</tr>
<tr>
<td>Icon</td>
<td>
<a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>
</td>
</tr>
</table>
 



The system automatically deletes these resources when the process that created them terminates; however, calling the appropriate function saves memory and decreases the size of the process's working set.


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-window-classes">Using Window Classes</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines LoadImage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-copyimage">CopyImage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadbitmapa">LoadBitmap</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/menurc/resources">Resources</a>
