---
UID: NF:wingdi.SetMetaFileBitsEx
title: SetMetaFileBitsEx function (wingdi.h)
description: The SetMetaFileBitsEx function creates a memory-based Windows-format metafile from the supplied data.
helpviewer_keywords: ["SetMetaFileBitsEx","SetMetaFileBitsEx function [Windows GDI]","_win32_SetMetaFileBitsEx","gdi.setmetafilebitsex","wingdi/SetMetaFileBitsEx"]
old-location: gdi\setmetafilebitsex.htm
tech.root: gdi
ms.assetid: 232eeba9-f579-4b5f-a31a-416aeb56a909
ms.date: 12/05/2018
ms.keywords: SetMetaFileBitsEx, SetMetaFileBitsEx function [Windows GDI], _win32_SetMetaFileBitsEx, gdi.setmetafilebitsex, wingdi/SetMetaFileBitsEx
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
 - SetMetaFileBitsEx
 - wingdi/SetMetaFileBitsEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Metafile-l1-1-0.dll
 - Ext-MS-Win-GDI-Metafile-l1-1-1.dll
 - ext-ms-win-gdi-metafile-l1-1-2.dll
 - GDI32Full.dll
api_name:
 - SetMetaFileBitsEx
---

# SetMetaFileBitsEx function


## -description

The <b>SetMetaFileBitsEx</b> function creates a memory-based Windows-format metafile from the supplied data.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="/windows/desktop/api/wingdi/nf-wingdi-setenhmetafilebits">SetEnhMetaFileBits</a>.</div><div> </div>

## -parameters

### -param cbBuffer [in]

Specifies the size, in bytes, of the Windows-format metafile.

### -param lpData [in]

Pointer to a buffer that contains the Windows-format metafile. (It is assumed that the data was obtained by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-getmetafilebitsex">GetMetaFileBitsEx</a> function.)

## -returns

If the function succeeds, the return value is a handle to a memory-based Windows-format metafile.

If the function fails, the return value is <b>NULL</b>.

## -remarks

To convert a Windows-format metafile into an enhanced-format metafile, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a> function.

When the application no longer needs the metafile handle returned by <b>SetMetaFileBitsEx</b>, it should delete it by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletemetafile">DeleteMetaFile</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-deletemetafile">DeleteMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getmetafilebitsex">GetMetaFileBitsEx</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setenhmetafilebits">SetEnhMetaFileBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a>