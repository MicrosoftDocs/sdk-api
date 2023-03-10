---
UID: NF:winuser.CreateIcon
title: CreateIcon function (winuser.h)
description: Creates an icon that has the specified size, colors, and bit patterns.
helpviewer_keywords: ["CreateIcon","CreateIcon function [Menus and Other Resources]","_win32_CreateIcon","_win32_createicon_cpp","menurc.createicon","winui._win32_createicon","winuser/CreateIcon"]
old-location: menurc\createicon.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\createicon.htm
ms.date: 12/05/2018
ms.keywords: CreateIcon, CreateIcon function [Menus and Other Resources], _win32_CreateIcon, _win32_createicon_cpp, menurc.createicon, winui._win32_createicon, winuser/CreateIcon
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
 - CreateIcon
 - winuser/CreateIcon
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
 - CreateIcon
---

# CreateIcon function

## -description

Creates an icon that has the specified size, colors, and bit patterns.

To create a colored icon at run time you can use the [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) function, which creates a icon based on the content of an [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) structure.

## -parameters

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the instance of the module creating the icon.

### -param nWidth [in]

Type: <b>int</b>

The width, in pixels, of the icon.

### -param nHeight [in]

Type: <b>int</b>

The height, in pixels, of the icon.

### -param cPlanes [in]

Type: <b>BYTE</b>

The number of planes in the XOR bitmask of the icon.

### -param cBitsPixel [in]

Type: <b>BYTE</b>

The number of bits-per-pixel in the XOR bitmask of the icon.

### -param lpbANDbits [in]

Type: <b>const BYTE*</b>

An array of bytes that contains the bit values for the AND bitmask of the icon. This bitmask describes a monochrome bitmap.

### -param lpbXORbits [in]

Type: <b>const BYTE*</b>

An array of bytes that contains the bit values for the XOR bitmask of the icon. This bitmask describes a monochrome or device-dependent color bitmap.

## -returns

Type: <b>HICON</b>

If the function succeeds, the return value is a handle to an icon.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For more information about <i>nWidth</i> and <i>nHeight</i> parameters see <a href="/windows/desktop/menurc/about-icons#icon-sizes">Icon Sizes</a>. 

<b>CreateIcon</b> applies the following truth table to the AND and XOR bitmasks.

<table class="clsStd">
<tr>
<th>AND bitmask</th>
<th>XOR bitmask</th>
<th>Display</th>
</tr>
<tr>
<td>0</td>
<td>0</td>
<td>Black </td>
</tr>
<tr>
<td>0</td>
<td>1</td>
<td>White </td>
</tr>
<tr>
<td>1</td>
<td>0</td>
<td>Screen </td>
</tr>
<tr>
<td>1</td>
<td>1</td>
<td>Reverse screen </td>
</tr>
</table>

When you are finished using the icon, destroy it using the <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> function.

#### Examples

For an example, see <a href="/windows/desktop/menurc/using-icons">Creating an Icon</a>.

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/Winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>

<a href="/windows/desktop/menurc/icons">Icons</a>

<a href="/windows/desktop/menurc/about-icons#icon-sizes">Icon Sizes</a>

<b>Other Resources</b>
