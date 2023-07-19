---
UID: NS:wingdi.tagEMRGDICOMMENT
title: EMRGDICOMMENT (wingdi.h)
description: The EMRGDICOMMENT structure contains application-specific data.
helpviewer_keywords: ["*PEMRGDICOMMENT","EMRGDICOMMENT","EMRGDICOMMENT structure [Windows GDI]","PEMRGDICOMMENT","PEMRGDICOMMENT structure pointer [Windows GDI]","_win32_EMRGDICOMMENT_str","gdi.emrgdicomment","wingdi/EMRGDICOMMENT","wingdi/PEMRGDICOMMENT"]
old-location: gdi\emrgdicomment.htm
tech.root: gdi
ms.assetid: aac18154-bd50-45a4-a1ba-390b59525fa9
ms.date: 12/05/2018
ms.keywords: '*PEMRGDICOMMENT, EMRGDICOMMENT, EMRGDICOMMENT structure [Windows GDI], PEMRGDICOMMENT, PEMRGDICOMMENT structure pointer [Windows GDI], _win32_EMRGDICOMMENT_str, gdi.emrgdicomment, wingdi/EMRGDICOMMENT, wingdi/PEMRGDICOMMENT'
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
req.typenames: EMRGDICOMMENT, *PEMRGDICOMMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRGDICOMMENT
 - wingdi/tagEMRGDICOMMENT
 - PEMRGDICOMMENT
 - wingdi/PEMRGDICOMMENT
 - EMRGDICOMMENT
 - wingdi/EMRGDICOMMENT
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
 - EMRGDICOMMENT
---

# EMRGDICOMMENT structure


## -description

The <b>EMRGDICOMMENT</b> structure contains application-specific data. This enhanced metafile record is only meaningful to applications that know the format of the data and how to utilize it. This record is ignored by graphics device interface (GDI) during playback of the enhanced metafile.

## -struct-fields

### -field emr

The base structure for all record types.

### -field cbData

Size of data buffer, in bytes.

### -field Data

Application-specific data.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>
