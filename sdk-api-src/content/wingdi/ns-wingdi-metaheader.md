---
UID: NS:wingdi.tagMETAHEADER
title: METAHEADER (wingdi.h)
description: The METAHEADER structure contains information about a Windows-format metafile.
helpviewer_keywords: ["*LPMETAHEADER","*PMETAHEADER","METAHEADER","METAHEADER structure [Windows GDI]","PMETAHEADER","PMETAHEADER structure pointer [Windows GDI]","_win32_METAHEADER_str","gdi.metaheader","wingdi/METAHEADER","wingdi/PMETAHEADER"]
old-location: gdi\metaheader.htm
tech.root: gdi
ms.assetid: 3ad5be24-9558-442e-8c77-dd6a7d33c208
ms.date: 12/05/2018
ms.keywords: '*LPMETAHEADER, *PMETAHEADER, METAHEADER, METAHEADER structure [Windows GDI], PMETAHEADER, PMETAHEADER structure pointer [Windows GDI], _win32_METAHEADER_str, gdi.metaheader, wingdi/METAHEADER, wingdi/PMETAHEADER'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: METAHEADER, *PMETAHEADER, *LPMETAHEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMETAHEADER
 - wingdi/tagMETAHEADER
 - PMETAHEADER
 - wingdi/PMETAHEADER
 - METAHEADER
 - wingdi/METAHEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - METAHEADER
---

# METAHEADER structure


## -description

The <b>METAHEADER</b> structure contains information about a Windows-format metafile.

## -struct-fields

### -field mtType

Specifies whether the metafile is in memory or recorded in a disk file. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>1</td>
<td>Metafile is in memory.</td>
</tr>
<tr>
<td>2</td>
<td>Metafile is in a disk file.</td>
</tr>
</table>

### -field mtHeaderSize

The size, in words, of the metafile header.

### -field mtVersion

The system version number. The version number for metafiles that support device-independent bitmaps (DIBs) is 0x0300. Otherwise, the version number is 0x0100.

### -field mtSize

The size, in words, of the file.

### -field mtNoObjects

The maximum number of objects that exist in the metafile at the same time.

### -field mtMaxRecord

The size, in words, of the largest record in the metafile.

### -field mtNoParameters

Reserved.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-metarecord">METARECORD</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>