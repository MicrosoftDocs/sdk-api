---
UID: NF:winuser.CreateIconFromResourceEx
title: CreateIconFromResourceEx function (winuser.h)
description: Creates an icon or cursor from resource bits describing the icon. (CreateIconFromResourceEx)
helpviewer_keywords: ["CreateIconFromResourceEx","CreateIconFromResourceEx function [Menus and Other Resources]","LR_DEFAULTCOLOR","LR_DEFAULTSIZE","LR_MONOCHROME","LR_SHARED","_win32_CreateIconFromResourceEx","_win32_createiconfromresourceex_cpp","menurc.createiconfromresourceex","winui._win32_createiconfromresourceex","winuser/CreateIconFromResourceEx"]
old-location: menurc\createiconfromresourceex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\createiconfromresourceex.htm
ms.date: 12/05/2018
ms.keywords: CreateIconFromResourceEx, CreateIconFromResourceEx function [Menus and Other Resources], LR_DEFAULTCOLOR, LR_DEFAULTSIZE, LR_MONOCHROME, LR_SHARED, _win32_CreateIconFromResourceEx, _win32_createiconfromresourceex_cpp, menurc.createiconfromresourceex, winui._win32_createiconfromresourceex, winuser/CreateIconFromResourceEx
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
 - CreateIconFromResourceEx
 - winuser/CreateIconFromResourceEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - CreateIconFromResourceEx
---

# CreateIconFromResourceEx function


## -description

Creates an icon or cursor from resource bits describing the icon.

## -parameters

### -param presbits [in]

Type: <b>PBYTE</b>

The DWORD-aligned buffer pointer containing the icon (<b>RT_ICON</b>) or cursor (<b>RT_CURSOR</b>) resource bits. These bits are typically loaded by calls to the <a href="/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex">LookupIconIdFromDirectoryEx</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a> functions.

See <a href="/windows/win32/menurc/resource-file-formats#cursor-and-icon-resources">Cursor and Icon Resources</a> for more info on icon and cursor resource format.

### -param dwResSize [in]

Type: <b>DWORD</b>

The size, in bytes, of the set of bits pointed to by the <i>pbIconBits</i> parameter.

### -param fIcon [in]

Type: <b>BOOL</b>

Indicates whether an icon or a cursor is to be created. If this parameter is <b>TRUE</b>, an icon is to be created. If it is <b>FALSE</b>, a cursor is to be created.

The <a href="/windows/win32/menurc/localheader">LOCALHEADER</a> structure defines cursor hotspot and is the first data read from the cursor resource bits.

### -param dwVer [in]

Type: <b>DWORD</b>

The version number of the icon or cursor format for the resource bits pointed to by the <i>presbits</i> parameter. The value must be greater than or equal to 0x00020000 and less than or equal to 0x00030000. This parameter is generally set to 0x00030000.

### -param cxDesired [in]

Type: <b>int</b>

The width, in pixels, of the icon or cursor. If this parameter is zero and the <i>Flags</i> parameter is <b>LR_DEFAULTSIZE</b>, the function uses the <b>SM_CXICON</b> or <b>SM_CXCURSOR</b> system metric value to set the width. If this parameter is zero and <b>LR_DEFAULTSIZE</b> is not used, the function uses the actual resource width.

### -param cyDesired [in]

Type: <b>int</b>

The height, in pixels, of the icon or cursor. If this parameter is zero and the <i>Flags</i> parameter is <b>LR_DEFAULTSIZE</b>, the function uses the <b>SM_CYICON</b> or <b>SM_CYCURSOR</b> system metric value to set the height. If this parameter is zero and <b>LR_DEFAULTSIZE</b> is not used, the function uses the actual resource height.

### -param Flags [in]

Type: <b>UINT</b>

A combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LR_DEFAULTCOLOR"></a><a id="lr_defaultcolor"></a><dl>
<dt><b>LR_DEFAULTCOLOR</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Uses the default color format.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_DEFAULTSIZE"></a><a id="lr_defaultsize"></a><dl>
<dt><b>LR_DEFAULTSIZE</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Uses the width or height specified by the system metric values for cursors or icons, if the <i>cxDesired</i> or <i>cyDesired</i> values are set to zero. If this flag is not specified and <i>cxDesired</i> and <i>cyDesired</i> are set to zero, the function uses the actual resource size.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_MONOCHROME"></a><a id="lr_monochrome"></a><dl>
<dt><b>LR_MONOCHROME</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Creates a monochrome icon or cursor. 

</td>
</tr>
<tr>
<td width="40%"><a id="LR_SHARED"></a><a id="lr_shared"></a><dl>
<dt><b>LR_SHARED</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Shares the icon or cursor handle if the icon or cursor is created multiple times. If <b>LR_SHARED</b> is not set, a second call to <b>CreateIconFromResourceEx</b> for the same resource will create the icon or cursor again and return a different handle.

When you use this flag, the system will destroy the resource when it is no longer needed. 

Do not use <b>LR_SHARED</b> for icons or cursors that have non-standard sizes, that may change after loading, or that are loaded from a file.

</td>
</tr>
</table>

## -returns

Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the icon or cursor.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresource">CreateIconFromResource</a>, <b>CreateIconFromResourceEx</b>, <a href="/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>, <a href="/windows/desktop/api/winuser/nf-winuser-geticoninfo">GetIconInfo</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex">LookupIconIdFromDirectoryEx</a> functions allow shell applications and icon browsers to examine and use resources throughout the system. 

You should call <a href="/windows/win32/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> for icons or <a href="/windows/win32/api/winuser/nf-winuser-destroycursor">DestroyCursor</a> for cursors created with <b>CreateIconFromResourceEx</b>.

#### Examples

For an example, see <a href="/windows/desktop/menurc/using-icons#sharing-icon-resources">Sharing Icon Resources</a>.

## -see-also

<a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresource">CreateIconFromResource</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>



<a href="/windows/desktop/api/winuser/nf-winuser-geticoninfo">GetIconInfo</a>



<a href="/windows/desktop/menurc/icons">Icons</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a>



<a href="/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex">LookupIconIdFromDirectoryEx</a>



<b>Other Resources</b>



<b>Reference</b>
