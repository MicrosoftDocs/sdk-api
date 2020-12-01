---
UID: NF:wingdi.GetMetaFileBitsEx
title: GetMetaFileBitsEx function (wingdi.h)
description: The GetMetaFileBitsEx function retrieves the contents of a Windows-format metafile and copies them into the specified buffer.
helpviewer_keywords: ["GetMetaFileBitsEx","GetMetaFileBitsEx function [Windows GDI]","_win32_GetMetaFileBitsEx","gdi.getmetafilebitsex","wingdi/GetMetaFileBitsEx"]
old-location: gdi\getmetafilebitsex.htm
tech.root: gdi
ms.assetid: 6ca6de2e-79cb-4503-a0d7-f616b8e383eb
ms.date: 12/05/2018
ms.keywords: GetMetaFileBitsEx, GetMetaFileBitsEx function [Windows GDI], _win32_GetMetaFileBitsEx, gdi.getmetafilebitsex, wingdi/GetMetaFileBitsEx
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
 - GetMetaFileBitsEx
 - wingdi/GetMetaFileBitsEx
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
 - GetMetaFileBitsEx
---

# GetMetaFileBitsEx function


## -description

The <b>GetMetaFileBitsEx</b> function retrieves the contents of a Windows-format metafile and copies them into the specified buffer.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilebits">GetEnhMetaFileBits</a>.</div><div> </div>

## -parameters

### -param hMF [in]

A handle to a Windows-format metafile.

### -param cbBuffer [in]

The size, in bytes, of the buffer to receive the data.

### -param lpData [out]

A pointer to a buffer that receives the metafile data. The buffer must be sufficiently large to contain the data. If <i>lpvData</i> is <b>NULL</b>, the function returns the number of bytes required to hold the data.

## -returns

If the function succeeds and the buffer pointer is <b>NULL</b>, the return value is the number of bytes required for the buffer; if the function succeeds and the buffer pointer is a valid pointer, the return value is the number of bytes copied.

If the function fails, the return value is zero.

## -remarks

After the Windows-metafile bits are retrieved, they can be used to create a memory-based metafile by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-setmetafilebitsex">SetMetaFileBitsEx</a> function.

The <b>GetMetaFileBitsEx</b> function does not invalidate the metafile handle. An application must delete this handle by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletemetafile">DeleteMetaFile</a> function.

To convert a Windows-format metafile into an enhanced-format metafile, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-deletemetafile">DeleteMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilebits">GetEnhMetaFileBits</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setmetafilebitsex">SetMetaFileBitsEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a>