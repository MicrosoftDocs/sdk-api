---
UID: NF:winuser.LoadBitmapA
title: LoadBitmapA function (winuser.h)
description: The LoadBitmap function loads the specified bitmap resource from a module's executable file. (ANSI)
helpviewer_keywords: ["LoadBitmapA", "winuser/LoadBitmapA"]
old-location: gdi\loadbitmap.htm
tech.root: gdi
ms.assetid: 5eed5f78-deaf-4b23-986e-4802dc05936c
ms.date: 12/05/2018
ms.keywords: LoadBitmap, LoadBitmap function [Windows GDI], LoadBitmapA, LoadBitmapW, _win32_LoadBitmap, gdi.loadbitmap, winuser/LoadBitmap, winuser/LoadBitmapA, winuser/LoadBitmapW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadBitmapW (Unicode) and LoadBitmapA (ANSI)
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
 - LoadBitmapA
 - winuser/LoadBitmapA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - LoadBitmap
 - LoadBitmapA
 - LoadBitmapW
req.apiset: ext-ms-win-ntuser-draw-l1-1-1 (introduced in Windows 8.1)
---

# LoadBitmapA function


## -description

<p class="CCE_Message">[<b>LoadBitmap</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a> and <a href="/windows/desktop/api/winuser/nf-winuser-drawframecontrol">DrawFrameControl</a>.]

The <b>LoadBitmap</b> function loads the specified bitmap resource from a module's executable file.

## -parameters

### -param hInstance [in]

A handle to the instance of the module whose executable file contains the bitmap to be loaded.

### -param lpBitmapName [in]

A pointer to a null-terminated string that contains the name of the bitmap resource to be loaded. Alternatively, this parameter can consist of the resource identifier in the low-order word and zero in the high-order word. The <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro can be used to create this value.

## -returns

If the function succeeds, the return value is the handle to the specified bitmap.

If the function fails, the return value is <b>NULL</b>.

## -remarks

If the bitmap pointed to by the <i>lpBitmapName</i> parameter does not exist or there is insufficient memory to load the bitmap, the function fails.

<b>LoadBitmap</b> creates a compatible bitmap of the display, which cannot be selected to a printer. To load a bitmap that you can select to a printer, call <a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a> and specify LR_CREATEDIBSECTION to create a DIB section. A DIB section can be selected to any device.

An application can use the <b>LoadBitmap</b> function to access predefined bitmaps. To do so, the application must set the <i>hInstance</i> parameter to <b>NULL</b> and the <i>lpBitmapName</i> parameter to one of the following values.

<table>
<tr>
<th>Bitmap name</th>
<th>Bitmap name</th>
</tr>
<tr>
<td>OBM_BTNCORNERS</td>
<td>OBM_OLD_RESTORE</td>
</tr>
<tr>
<td>OBM_BTSIZE</td>
<td>OBM_OLD_RGARROW</td>
</tr>
<tr>
<td>OBM_CHECK</td>
<td>OBM_OLD_UPARROW</td>
</tr>
<tr>
<td>OBM_CHECKBOXES</td>
<td>OBM_OLD_ZOOM</td>
</tr>
<tr>
<td>OBM_CLOSE</td>
<td>OBM_REDUCE</td>
</tr>
<tr>
<td>OBM_COMBO</td>
<td>OBM_REDUCED</td>
</tr>
<tr>
<td>OBM_DNARROW</td>
<td>OBM_RESTORE</td>
</tr>
<tr>
<td>OBM_DNARROWD</td>
<td>OBM_RESTORED</td>
</tr>
<tr>
<td>OBM_DNARROWI</td>
<td>OBM_RGARROW</td>
</tr>
<tr>
<td>OBM_LFARROW</td>
<td>OBM_RGARROWD</td>
</tr>
<tr>
<td>OBM_LFARROWD</td>
<td>OBM_RGARROWI</td>
</tr>
<tr>
<td>OBM_LFARROWI</td>
<td>OBM_SIZE</td>
</tr>
<tr>
<td>OBM_MNARROW</td>
<td>OBM_UPARROW</td>
</tr>
<tr>
<td>OBM_OLD_CLOSE</td>
<td>OBM_UPARROWD</td>
</tr>
<tr>
<td>OBM_OLD_DNARROW</td>
<td>OBM_UPARROWI</td>
</tr>
<tr>
<td>OBM_OLD_LFARROW</td>
<td>OBM_ZOOM</td>
</tr>
<tr>
<td>OBM_OLD_REDUCE</td>
<td>OBM_ZOOMD</td>
</tr>
</table>
 

Bitmap names that begin with OBM_OLD represent bitmaps used by 16-bit versions of Windows earlier than 3.0.

For an application to use any of the OBM_ constants, the constant OEMRESOURCE must be defined before the Windows.h header file is included.

The application must call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete each bitmap handle returned by the <b>LoadBitmap</b> function.


#### Examples

For an example, see Example of Menu-Item Bitmaps in <a href="/windows/desktop/menurc/using-menus">Using Menus</a>.

<div class="code"></div>




> [!NOTE]
> The winuser.h header defines LoadBitmap as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createbitmap">CreateBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/winuser/nf-winuser-drawframecontrol">DrawFrameControl</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>
