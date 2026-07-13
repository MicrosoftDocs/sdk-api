---
UID: NF:wingdi.CreateDIBSection
title: CreateDIBSection function (wingdi.h)
description: The CreateDIBSection function creates a DIB that applications can write to directly.
helpviewer_keywords: ["CreateDIBSection","CreateDIBSection function [Windows GDI]","DIB_PAL_COLORS","DIB_RGB_COLORS","_win32_CreateDIBSection","gdi.createdibsection","wingdi/CreateDIBSection"]
old-location: gdi\createdibsection.htm
tech.root: gdi
ms.assetid: 9276ec84-2860-42be-a9f8-d4efb8d25eec
ms.date: 12/05/2018
ms.keywords: CreateDIBSection, CreateDIBSection function [Windows GDI], DIB_PAL_COLORS, DIB_RGB_COLORS, _win32_CreateDIBSection, gdi.createdibsection, wingdi/CreateDIBSection
req.header: wingdi.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateDIBSection
 - wingdi/CreateDIBSection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - CreateDIBSection
---

# CreateDIBSection function


## -description

The <b>CreateDIBSection</b> function creates a DIB that applications can write to directly. The function gives you a pointer to the location of the bitmap bit values. You can supply a handle to a file-mapping object that the function will use to create the bitmap, or you can let the system allocate the memory for the bitmap.

## -parameters

### -param hdc [in]

A handle to a device context. If the value of <i>iUsage</i> is DIB_PAL_COLORS, the function uses this device context's logical palette to initialize the DIB colors.

### -param pbmi [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure that specifies various attributes of the DIB, including the bitmap dimensions and colors.

### -param usage [in]

The type of data contained in the <b>bmiColors</b> array member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure pointed to by <i>pbmi</i> (either logical palette indexes or literal RGB values). The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DIB_PAL_COLORS"></a><a id="dib_pal_colors"></a><dl>
<dt><b>DIB_PAL_COLORS</b></dt>
</dl>
</td>
<td width="60%">
The <b>bmiColors</b> member is an array of 16-bit indexes into the logical palette of the device context specified by <i>hdc</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="DIB_RGB_COLORS"></a><a id="dib_rgb_colors"></a><dl>
<dt><b>DIB_RGB_COLORS</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure contains an array of literal RGB values.

</td>
</tr>
</table>

### -param ppvBits [out]

A pointer to a variable that receives a pointer to the location of the DIB bit values.

### -param hSection [in]

A handle to a file-mapping object that the function will use to create the DIB. This parameter can be <b>NULL</b>.

If <i>hSection</i> is not <b>NULL</b>, it must be a handle to a file-mapping object created by calling the <a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a> function with the PAGE_READWRITE or PAGE_WRITECOPY flag. Read-only DIB sections are not supported. Handles created by other means will cause <b>CreateDIBSection</b> to fail.

If <i>hSection</i> is not <b>NULL</b>, the <b>CreateDIBSection</b> function locates the bitmap bit values at offset <i>dwOffset</i> in the file-mapping object referred to by <i>hSection</i>. An application can later retrieve the <i>hSection</i> handle by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a> function with the <b>HBITMAP</b> returned by <b>CreateDIBSection</b>.

If <i>hSection</i> is <b>NULL</b>, the system allocates memory for the DIB. In this case, the <b>CreateDIBSection</b> function ignores the <i>dwOffset</i> parameter. An application cannot later obtain a handle to this memory. The <b>dshSection</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-dibsection">DIBSECTION</a> structure filled in by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a> function will be <b>NULL</b>.

### -param offset [in]

The offset from the beginning of the file-mapping object referenced by <i>hSection</i> where storage for the bitmap bit values is to begin. This value is ignored if <i>hSection</i> is <b>NULL</b>. The bitmap bit values are aligned on doubleword boundaries, so <i>dwOffset</i> must be a multiple of the size of a <b>DWORD</b>.

## -returns

If the function succeeds, the return value is a handle to the newly created DIB, and *<i>ppvBits</i> points to the bitmap bit values.

If the function fails, the return value is <b>NULL</b>, and *<i>ppvBits</i> is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> can return the following value:

<table>
<tr>
<th>Error code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input parameters is invalid.

</td>
</tr>
</table>

## -remarks

As noted above, if <i>hSection</i> is <b>NULL</b>, the system allocates memory for the DIB. The system closes the handle to that memory when you later delete the DIB by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function. If <i>hSection</i> is not <b>NULL</b>, you must close the <i>hSection</i> memory handle yourself after calling <b>DeleteObject</b> to delete the bitmap.

You cannot paste a DIB section from one application into another application.

<b>CreateDIBSection</b> does not use the <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> parameters <i>biXPelsPerMeter</i> or <i>biYPelsPerMeter</i> and will not provide resolution information in the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure.

You need to guarantee that the GDI subsystem has completed any drawing to a bitmap created by <b>CreateDIBSection</b> before you draw to the bitmap yourself. Access to the bitmap must be synchronized. Do this by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-gdiflush">GdiFlush</a> function. This applies to any use of the pointer to the bitmap bit values, including passing the pointer in calls to functions such as <a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>.

<b>ICM:</b> No color management is done.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-dibsection">DIBSECTION</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gdiflush">GdiFlush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibcolortable">GetDIBColorTable</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibcolortable">SetDIBColorTable</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>
