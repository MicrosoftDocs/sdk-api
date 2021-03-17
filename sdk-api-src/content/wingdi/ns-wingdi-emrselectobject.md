---
UID: NS:wingdi.tagEMRSELECTOBJECT
title: EMRSELECTOBJECT (wingdi.h)
description: The EMRSELECTOBJECT and EMRDELETEOBJECT structures contain members for the SelectObject and DeleteObject enhanced metafile records.
helpviewer_keywords: ["*PEMRDELETEOBJECT","*PEMRSELECTOBJECT","EMRDELETEOBJECT","EMRDELETEOBJECT structure [Windows GDI]","EMRSELECTOBJECT","EMRSELECTOBJECT structure [Windows GDI]","EMRSELECTOBJECT","EMRDELETEOBJECT","EMRSELECTOBJECT","EMRDELETEOBJECT structure [Windows GDI]","PEMRDELETEOBJECT","PEMRDELETEOBJECT structure pointer [Windows GDI]","PEMRSELECTOBJECT","PEMRSELECTOBJECT structure pointer [Windows GDI]","_win32_EMRSELECTOBJECT_str","gdi.emrselectobject__emrdeleteobject","wingdi/EMRDELETEOBJECT","wingdi/EMRSELECTOBJECT","EMRDELETEOBJECT","wingdi/PEMRDELETEOBJECT","wingdi/PEMRSELECTOBJECT"]
old-location: gdi\emrselectobject__emrdeleteobject.htm
tech.root: gdi
ms.assetid: 02ec5839-3390-429b-8f0c-6f2e74393c8f
ms.date: 12/05/2018
ms.keywords: '*PEMRDELETEOBJECT, *PEMRSELECTOBJECT, EMRDELETEOBJECT, EMRDELETEOBJECT structure [Windows GDI], EMRSELECTOBJECT, EMRSELECTOBJECT structure [Windows GDI], EMRSELECTOBJECT,EMRDELETEOBJECT, EMRSELECTOBJECT,EMRDELETEOBJECT structure [Windows GDI], PEMRDELETEOBJECT, PEMRDELETEOBJECT structure pointer [Windows GDI], PEMRSELECTOBJECT, PEMRSELECTOBJECT structure pointer [Windows GDI], _win32_EMRSELECTOBJECT_str, gdi.emrselectobject__emrdeleteobject, wingdi/EMRDELETEOBJECT, wingdi/EMRSELECTOBJECT,EMRDELETEOBJECT, wingdi/PEMRDELETEOBJECT, wingdi/PEMRSELECTOBJECT'
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
req.typenames: EMRSELECTOBJECT, *PEMRSELECTOBJECT, EMRDELETEOBJECT, *PEMRDELETEOBJECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSELECTOBJECT
 - wingdi/tagEMRSELECTOBJECT
 - PEMRSELECTOBJECT
 - wingdi/PEMRSELECTOBJECT
 - EMRSELECTOBJECT
 - wingdi/EMRSELECTOBJECT
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
 - EMRSELECTOBJECT
---

# EMRSELECTOBJECT structure


## -description

The <b>EMRSELECTOBJECT</b> and <b>EMRDELETEOBJECT</b> structures contain members for the <b>SelectObject</b> and <b>DeleteObject</b> enhanced metafile records.

## -struct-fields

### -field emr

The base structure for all record types.

### -field ihObject

The index of an object in the handle table.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-emr">EMR</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getstockobject">GetStockObject</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>