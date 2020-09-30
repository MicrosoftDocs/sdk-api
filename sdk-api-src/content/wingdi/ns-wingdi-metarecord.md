---
UID: NS:wingdi.tagMETARECORD
title: METARECORD (wingdi.h)
description: The METARECORD structure contains a Windows-format metafile record.
helpviewer_keywords: ["*LPMETARECORD","*PMETARECORD","METARECORD","METARECORD structure [Windows GDI]","PMETARECORD","PMETARECORD structure pointer [Windows GDI]","_win32_METARECORD_str","gdi.metarecord","wingdi/METARECORD","wingdi/PMETARECORD"]
old-location: gdi\metarecord.htm
tech.root: gdi
ms.assetid: 7c5d6e97-dff1-4c80-a7d3-082413dca469
ms.date: 12/05/2018
ms.keywords: '*LPMETARECORD, *PMETARECORD, METARECORD, METARECORD structure [Windows GDI], PMETARECORD, PMETARECORD structure pointer [Windows GDI], _win32_METARECORD_str, gdi.metarecord, wingdi/METARECORD, wingdi/PMETARECORD'
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
req.typenames: METARECORD, *PMETARECORD, *LPMETARECORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMETARECORD
 - wingdi/tagMETARECORD
 - PMETARECORD
 - wingdi/PMETARECORD
 - METARECORD
 - wingdi/METARECORD
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
 - METARECORD
---

# METARECORD structure


## -description

The <b>METARECORD</b> structure contains a Windows-format metafile record.

## -struct-fields

### -field rdSize

The size, in words, of the record.

### -field rdFunction

The function number.

### -field rdParm

An array of words containing the function parameters, in reverse of the order they are passed to the function.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-metaheader">METAHEADER</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>