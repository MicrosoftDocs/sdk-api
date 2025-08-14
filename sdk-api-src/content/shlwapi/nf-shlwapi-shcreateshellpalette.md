---
UID: NF:shlwapi.SHCreateShellPalette
title: SHCreateShellPalette function (shlwapi.h)
description: Creates a halftone palette for the specified device context.
helpviewer_keywords: ["SHCreateShellPalette","SHCreateShellPalette function [Windows Shell]","_win32_SHCreateShellPalette","shell.SHCreateShellPalette","shlwapi/SHCreateShellPalette"]
old-location: shell\SHCreateShellPalette.htm
tech.root: shell
ms.assetid: 49afb04a-34e3-4696-a046-bc9308ae7adf
ms.date: 12/05/2018
ms.keywords: SHCreateShellPalette, SHCreateShellPalette function [Windows Shell], _win32_SHCreateShellPalette, shell.SHCreateShellPalette, shlwapi/SHCreateShellPalette
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateShellPalette
 - shlwapi/SHCreateShellPalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - Ext-MS-Win-Shell-ShlwApi-l1-1-1.dll
 - Ext-MS-Win-Shell-ShlwAPI-L1-1-2.dll
api_name:
 - SHCreateShellPalette
---

# SHCreateShellPalette function


## -description

Creates a halftone palette for the specified device context.

## -parameters

### -param hdc [in, optional]

Type: <b>HDC</b>

The device context.

## -returns

Type: <b>HPALETTE</b>

Returns the palette if successful; otherwise 0.

## -remarks

This function behaves the same as <a href="/windows/desktop/api/wingdi/nf-wingdi-createhalftonepalette">CreateHalftonePalette</a>. The palette that is returned depends on the device context in the following way:

				

<ul>
<li>If <i>hdc</i> is set to <b>NULL</b>, a full palette is returned.</li>
<li>If the device context is indexed, a full palette is returned.</li>
<li>If the device context is not indexed, a default palette (VGA colors) is returned.</li>
</ul>