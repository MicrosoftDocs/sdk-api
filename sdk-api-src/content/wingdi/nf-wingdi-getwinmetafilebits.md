---
UID: NF:wingdi.GetWinMetaFileBits
title: GetWinMetaFileBits function (wingdi.h)
description: The GetWinMetaFileBits function converts the enhanced-format records from a metafile into Windows-format records and stores the converted records in the specified buffer.
helpviewer_keywords: ["GetWinMetaFileBits","GetWinMetaFileBits function [Windows GDI]","_win32_GetWinMetaFileBits","gdi.getwinmetafilebits","wingdi/GetWinMetaFileBits"]
old-location: gdi\getwinmetafilebits.htm
tech.root: gdi
ms.assetid: db61ea3a-44d0-4769-acb4-05a982d3f06f
ms.date: 12/05/2018
ms.keywords: GetWinMetaFileBits, GetWinMetaFileBits function [Windows GDI], _win32_GetWinMetaFileBits, gdi.getwinmetafilebits, wingdi/GetWinMetaFileBits
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
 - GetWinMetaFileBits
 - wingdi/GetWinMetaFileBits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Metafile-l1-1-1.dll
 - ext-ms-win-gdi-metafile-l1-1-2.dll
 - GDI32Full.dll
api_name:
 - GetWinMetaFileBits
---

# GetWinMetaFileBits function


## -description

The <b>GetWinMetaFileBits</b> function converts the enhanced-format records from a metafile into Windows-format records and stores the converted records in the specified buffer.

## -parameters

### -param hemf [in]

A handle to the enhanced metafile.

### -param cbData16 [in]

The size, in bytes, of the buffer into which the converted records are to be copied.

### -param pData16 [out]

A pointer to the buffer that receives the converted records. If <i>lpbBuffer</i> is <b>NULL</b>, <b>GetWinMetaFileBits</b> returns the number of bytes required to store the converted metafile records.

### -param iMapMode [in]

The mapping mode to use in the converted metafile.

### -param hdcRef [in]

A handle to the reference device context.

## -returns

If the function succeeds and the buffer pointer is <b>NULL</b>, the return value is the number of bytes required to store the converted records; if the function succeeds and the buffer pointer is a valid pointer, the return value is the size of the metafile data in bytes.

If the function fails, the return value is zero.

## -remarks

This function converts an enhanced metafile into a Windows-format metafile so that its picture can be displayed in an application that recognizes the older format.

The system uses the reference device context to determine the resolution of the converted metafile.

The <b>GetWinMetaFileBits</b> function does not invalidate the enhanced metafile handle. An application should call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a> function to release the handle when it is no longer needed.

To create a scalable Windows-format metafile, specify MM_ANISOTROPIC as the <i>fnMapMode</i> parameter.

The upper-left corner of the metafile picture is always mapped to the origin of the reference device.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setmapmode">SetMapMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a>