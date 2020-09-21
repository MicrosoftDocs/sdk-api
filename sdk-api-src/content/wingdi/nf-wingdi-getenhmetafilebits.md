---
UID: NF:wingdi.GetEnhMetaFileBits
title: GetEnhMetaFileBits function (wingdi.h)
description: The GetEnhMetaFileBits function retrieves the contents of the specified enhanced-format metafile and copies them into a buffer.
helpviewer_keywords: ["GetEnhMetaFileBits","GetEnhMetaFileBits function [Windows GDI]","_win32_GetEnhMetaFileBits","gdi.getenhmetafilebits","wingdi/GetEnhMetaFileBits"]
old-location: gdi\getenhmetafilebits.htm
tech.root: gdi
ms.assetid: 2bbfa0da-5b1e-4843-9777-c2e4c5fd3b78
ms.date: 12/05/2018
ms.keywords: GetEnhMetaFileBits, GetEnhMetaFileBits function [Windows GDI], _win32_GetEnhMetaFileBits, gdi.getenhmetafilebits, wingdi/GetEnhMetaFileBits
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
 - GetEnhMetaFileBits
 - wingdi/GetEnhMetaFileBits
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
 - GetEnhMetaFileBits
---

# GetEnhMetaFileBits function


## -description

The <b>GetEnhMetaFileBits</b> function retrieves the contents of the specified enhanced-format metafile and copies them into a buffer.

## -parameters

### -param hEMF [in]

A handle to the enhanced metafile.

### -param nSize [in]

The size, in bytes, of the buffer to receive the data.

### -param lpData [out]

A pointer to a buffer that receives the metafile data. The buffer must be sufficiently large to contain the data. If <i>lpbBuffer</i> is <b>NULL</b>, the function returns the size necessary to hold the data.

## -returns

If the function succeeds and the buffer pointer is <b>NULL</b>, the return value is the size of the enhanced metafile, in bytes.

If the function succeeds and the buffer pointer is a valid pointer, the return value is the number of bytes copied to the buffer.

If the function fails, the return value is zero.

## -remarks

After the enhanced-metafile bits are retrieved, they can be used to create a memory-based metafile by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-setenhmetafilebits">SetEnhMetaFileBits</a> function.

The <b>GetEnhMetaFileBits</b> function does not invalidate the enhanced-metafile handle. The application must call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a> function to delete the handle when it is no longer needed.

The metafile contents retrieved by this function are in the enhanced format. To retrieve the metafile contents in the Windows format, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-getwinmetafilebits">GetWinMetaFileBits</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getwinmetafilebits">GetWinMetaFileBits</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setenhmetafilebits">SetEnhMetaFileBits</a>