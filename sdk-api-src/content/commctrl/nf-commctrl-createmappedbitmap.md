---
UID: NF:commctrl.CreateMappedBitmap
title: CreateMappedBitmap function (commctrl.h)
description: Creates a bitmap for use in a toolbar.
helpviewer_keywords: ["CMB_MASKED","CreateMappedBitmap","CreateMappedBitmap function [Windows Controls]","_win32_CreateMappedBitmap","_win32_CreateMappedBitmap_cpp","commctrl/CreateMappedBitmap","controls.CreateMappedBitmap","controls._win32_CreateMappedBitmap"]
old-location: controls\CreateMappedBitmap.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\functions\createmappedbitmap.htm
ms.date: 12/05/2018
ms.keywords: CMB_MASKED, CreateMappedBitmap, CreateMappedBitmap function [Windows Controls], _win32_CreateMappedBitmap, _win32_CreateMappedBitmap_cpp, commctrl/CreateMappedBitmap, controls.CreateMappedBitmap, controls._win32_CreateMappedBitmap
req.header: commctrl.h
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateMappedBitmap
 - commctrl/CreateMappedBitmap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
 - Ext-MS-Win-Shell-ComCtl32-Init-L1-1-1.dll
api_name:
 - CreateMappedBitmap
req.apiset: ext-ms-win-shell-comctl32-init-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# CreateMappedBitmap function


## -description

Creates a bitmap for use in a toolbar.

## -parameters

### -param hInstance

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

Handle to the module instance with the executable file that contains the bitmap resource.

### -param idBitmap

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT_PTR</a></b>

Resource identifier of the bitmap resource.

### -param wFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Bitmap flag. This parameter can be zero or the following value: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMB_MASKED"></a><a id="cmb_masked"></a><dl>
<dt><b>CMB_MASKED</b></dt>
</dl>
</td>
<td width="60%">
Uses a bitmap as a mask.

</td>
</tr>
</table>

### -param lpColorMap [in]

Type: <b>LPCOLORMAP</b>

Pointer to a <a href="/windows/desktop/api/commctrl/ns-commctrl-colormap">COLORMAP</a> structure that contains the color information needed to map the bitmaps. If this parameter is <b>NULL</b>, the function uses the default color map.

### -param iNumMaps

Type: <b>int</b>

Number of color maps pointed to by 
					<i>lpColorMap</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HBITMAP</a></b>

Returns the handle to the bitmap if successful, or <b>NULL</b> otherwise. To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The function creates a new bitmap using the bitmap data and colors specified by the bitmap resource and the color mapping information. 

This function is fully supported only for images with color maps; that is, images with 256 or fewer colors.


#### Examples

The following example code creates a bitmap from a resource and makes the color black appear transparent by mapping it to the system color for a button face.


```cpp
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
```
