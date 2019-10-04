---
UID: NS:wingdi.tagENHMETARECORD
title: ENHMETARECORD (wingdi.h)
author: windows-sdk-content
description: The ENHMETARECORD structure contains data that describes a graphics device interface (GDI) function used to create part of a picture in an enhanced-format metafile.
old-location: gdi\enhmetarecord.htm
tech.root: gdi
ms.assetid: efe49094-fe61-40e1-873e-3302c595717e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPENHMETARECORD, *PENHMETARECORD, ENHMETARECORD, ENHMETARECORD structure [Windows GDI], PENHMETARECORD, PENHMETARECORD structure pointer [Windows GDI], _win32_ENHMETARECORD_str, gdi.enhmetarecord, wingdi/ENHMETARECORD, wingdi/PENHMETARECORD"
ms.topic: struct
f1_keywords: 
 - "wingdi/ENHMETARECORD"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - ENHMETARECORD
targetos: Windows
req.typenames: ENHMETARECORD, *PENHMETARECORD, *LPENHMETARECORD
req.redist: 
ms.custom: 19H1
---

# ENHMETARECORD structure


## -description



The <b>ENHMETARECORD</b> structure contains data that describes a graphics device interface (GDI) function used to create part of a picture in an enhanced-format metafile.




## -struct-fields




### -field iType

The record type.


### -field nSize

The size of the record, in bytes.


### -field dParm

An array of parameters passed to the GDI function identified by the record.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-enhmetaheader">ENHMETAHEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>
 

 

