---
UID: NF:wingdi.PlayMetaFileRecord
title: PlayMetaFileRecord function (wingdi.h)
description: The PlayMetaFileRecord function plays a Windows-format metafile record by executing the graphics device interface (GDI) function contained within that record.
helpviewer_keywords: ["PlayMetaFileRecord","PlayMetaFileRecord function [Windows GDI]","_win32_PlayMetaFileRecord","gdi.playmetafilerecord","wingdi/PlayMetaFileRecord"]
old-location: gdi\playmetafilerecord.htm
tech.root: gdi
ms.assetid: bea22981-dc77-4de2-b6dc-d6a4f4b74bbd
ms.date: 12/05/2018
ms.keywords: PlayMetaFileRecord, PlayMetaFileRecord function [Windows GDI], _win32_PlayMetaFileRecord, gdi.playmetafilerecord, wingdi/PlayMetaFileRecord
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
 - PlayMetaFileRecord
 - wingdi/PlayMetaFileRecord
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
 - PlayMetaFileRecord
---

# PlayMetaFileRecord function


## -description

The <b>PlayMetaFileRecord</b> function plays a Windows-format metafile record by executing the graphics device interface (GDI) function contained within that record.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="/windows/desktop/api/wingdi/nf-wingdi-playenhmetafilerecord">PlayEnhMetaFileRecord</a>.</div><div> </div>

## -parameters

### -param hdc [in]

A handle to a device context.

### -param lpHandleTable [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-handletable">HANDLETABLE</a> structure representing the table of handles to GDI objects used when playing the metafile.

### -param lpMR [in]

A pointer to the Windows-format metafile record.

### -param noObjs [in]

The number of handles in the handle table.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

To convert a Windows-format metafile into an enhanced-format metafile, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a> function.

An application typically uses <b>PlayMetaFileRecord</b> in conjunction with the <a href="/windows/desktop/api/wingdi/nf-wingdi-enummetafile">EnumMetaFile</a> function to process and play a Windows-format metafile one record at a time.

The <i>lpHandletable</i> and <i>nHandles</i> parameters must be identical to those passed to the <a href="/previous-versions/dd162630(v=vs.85)">EnumMetaFileProc</a> callback procedure by <a href="/windows/desktop/api/wingdi/nf-wingdi-enummetafile">EnumMetaFile</a>.

If the <b>PlayMetaFileRecord</b> function does not recognize a record, it ignores the record and returns <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-enummetafile">EnumMetaFile</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-handletable">HANDLETABLE</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-metarecord">METARECORD</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-playmetafile">PlayMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a>