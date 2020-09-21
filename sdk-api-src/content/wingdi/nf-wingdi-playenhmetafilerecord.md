---
UID: NF:wingdi.PlayEnhMetaFileRecord
title: PlayEnhMetaFileRecord function (wingdi.h)
description: The PlayEnhMetaFileRecord function plays an enhanced-metafile record by executing the graphics device interface (GDI) functions identified by the record.
helpviewer_keywords: ["PlayEnhMetaFileRecord","PlayEnhMetaFileRecord function [Windows GDI]","_win32_PlayEnhMetaFileRecord","gdi.playenhmetafilerecord","wingdi/PlayEnhMetaFileRecord"]
old-location: gdi\playenhmetafilerecord.htm
tech.root: gdi
ms.assetid: 3eec8c8d-b99f-4500-9d18-b819c097f341
ms.date: 12/05/2018
ms.keywords: PlayEnhMetaFileRecord, PlayEnhMetaFileRecord function [Windows GDI], _win32_PlayEnhMetaFileRecord, gdi.playenhmetafilerecord, wingdi/PlayEnhMetaFileRecord
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
 - PlayEnhMetaFileRecord
 - wingdi/PlayEnhMetaFileRecord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - PlayEnhMetaFileRecord
---

# PlayEnhMetaFileRecord function


## -description

The <b>PlayEnhMetaFileRecord</b> function plays an enhanced-metafile record by executing the graphics device interface (GDI) functions identified by the record.

## -parameters

### -param hdc [in]

A handle to the device context passed to the <a href="/windows/desktop/api/wingdi/nf-wingdi-enumenhmetafile">EnumEnhMetaFile</a> function.

### -param pht [in]

A pointer to a table of handles to GDI objects used when playing the metafile. The first entry in this table contains the enhanced-metafile handle.

### -param pmr [in]

A pointer to the enhanced-metafile record to be played.

### -param cht [in]

The number of handles in the handle table.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

This is an enhanced-metafile function.

An application typically uses <b>PlayEnhMetaFileRecord</b> in conjunction with the <a href="/windows/desktop/api/wingdi/nf-wingdi-enumenhmetafile">EnumEnhMetaFile</a> function to process and play an enhanced-format metafile one record at a time.

The <i>hdc</i>, <i>lpHandletable</i>, and <i>nHandles</i> parameters must be exactly those passed to the <a href="/previous-versions/dd162606(v=vs.85)">EnhMetaFileProc</a> callback procedure by the <a href="/windows/desktop/api/wingdi/nf-wingdi-enumenhmetafile">EnumEnhMetaFile</a> function.

If <b>PlayEnhMetaFileRecord</b> does not recognize a record, it ignores the record and returns <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-enumenhmetafile">EnumEnhMetaFile</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-playenhmetafile">PlayEnhMetaFile</a>