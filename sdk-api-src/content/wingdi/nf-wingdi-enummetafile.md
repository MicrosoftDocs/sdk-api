---
UID: NF:wingdi.EnumMetaFile
title: EnumMetaFile function (wingdi.h)
description: The EnumMetaFile function enumerates the records within a Windows-format metafile by retrieving each record and passing it to the specified callback function.
helpviewer_keywords: ["EnumMetaFile","EnumMetaFile function [Windows GDI]","_win32_EnumMetaFile","gdi.enummetafile","wingdi/EnumMetaFile"]
old-location: gdi\enummetafile.htm
tech.root: gdi
ms.assetid: b11c7467-64a9-442b-8dee-26e15f64a26b
ms.date: 12/05/2018
ms.keywords: EnumMetaFile, EnumMetaFile function [Windows GDI], _win32_EnumMetaFile, gdi.enummetafile, wingdi/EnumMetaFile
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
 - EnumMetaFile
 - wingdi/EnumMetaFile
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
 - EnumMetaFile
---

# EnumMetaFile function


## -description

The <b>EnumMetaFile</b> function enumerates the records within a Windows-format metafile by retrieving each record and passing it to the specified callback function. The application-supplied callback function processes each record as required. The enumeration continues until the last record is processed or when the callback function returns zero.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="/windows/desktop/api/wingdi/nf-wingdi-enumenhmetafile">EnumEnhMetaFile</a>.</div><div> </div>

## -parameters

### -param hdc [in]

Handle to a device context. This handle is passed to the callback function.

### -param hmf [in]

Handle to a Windows-format metafile.

### -param proc [in]

Pointer to an application-supplied callback function. For more information, see <a href="/previous-versions/dd162630(v=vs.85)">EnumMetaFileProc</a>.

### -param param [in]

Pointer to optional data.

## -returns

If the callback function successfully enumerates all the records in the Windows-format metafile, the return value is nonzero.

If the callback function does not successfully enumerate all the records in the Windows-format metafile, the return value is zero.

## -remarks

To convert a Windows-format metafile into an enhanced-format metafile, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a> function.

You can use the <b>EnumMetaFile</b> function to embed one Windows-format metafile within another.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-enumenhmetafile">EnumEnhMetaFile</a>



<a href="/previous-versions/dd162630(v=vs.85)">EnumMetaFileProc</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-playmetafile">PlayMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-playmetafilerecord">PlayMetaFileRecord</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwinmetafilebits">SetWinMetaFileBits</a>