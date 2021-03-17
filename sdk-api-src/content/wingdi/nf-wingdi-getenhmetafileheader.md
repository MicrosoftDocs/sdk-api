---
UID: NF:wingdi.GetEnhMetaFileHeader
title: GetEnhMetaFileHeader function (wingdi.h)
description: The GetEnhMetaFileHeader function retrieves the record containing the header for the specified enhanced-format metafile.
helpviewer_keywords: ["GetEnhMetaFileHeader","GetEnhMetaFileHeader function [Windows GDI]","_win32_GetEnhMetaFileHeader","gdi.getenhmetafileheader","wingdi/GetEnhMetaFileHeader"]
old-location: gdi\getenhmetafileheader.htm
tech.root: gdi
ms.assetid: c42bcbe2-2e8f-42bd-a8e3-2827c6563300
ms.date: 12/05/2018
ms.keywords: GetEnhMetaFileHeader, GetEnhMetaFileHeader function [Windows GDI], _win32_GetEnhMetaFileHeader, gdi.getenhmetafileheader, wingdi/GetEnhMetaFileHeader
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
 - GetEnhMetaFileHeader
 - wingdi/GetEnhMetaFileHeader
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
 - GetEnhMetaFileHeader
---

# GetEnhMetaFileHeader function


## -description

The <b>GetEnhMetaFileHeader</b> function retrieves the record containing the header for the specified enhanced-format metafile.

## -parameters

### -param hemf [in]

A handle to the enhanced metafile for which the header is to be retrieved.

### -param nSize [in]

The size, in bytes, of the buffer to receive the data. Only this many bytes will be copied.

### -param lpEnhMetaHeader [out]

A pointer to an <a href="/windows/desktop/api/wingdi/ns-wingdi-enhmetaheader">ENHMETAHEADER</a> structure that receives the header record. If this parameter is <b>NULL</b>, the function returns the size of the header record.

## -returns

If the function succeeds and the structure pointer is <b>NULL</b>, the return value is the size of the record that contains the header; if the structure pointer is a valid pointer, the return value is the number of bytes copied. Otherwise, it is zero.

## -remarks

An enhanced-metafile header contains such information as the metafile's size, in bytes; the dimensions of the picture stored in the metafile; the number of records stored in the metafile; the offset to the optional text description; the size of the optional palette, and the resolution of the device on which the picture was created.

The record that contains the enhanced-metafile header is always the first record in the metafile.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-enhmetaheader">ENHMETAHEADER</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-playenhmetafile">PlayEnhMetaFile</a>