---
UID: NS:wingdi.tagEMRSETCOLORSPACE
title: EMRSETCOLORSPACE (wingdi.h)
description: The EMRSETCOLORSPACE, EMRSELECTCOLORSPACE, and EMRDELETECOLORSPACE structures contain members for the SetColorSpace and DeleteColorSpace enhanced metafile records.
helpviewer_keywords: ["*PEMRDELETECOLORSPACE","*PEMRSELECTCOLORSPACE","*PEMRSETCOLORSPACE","EMRDELETECOLORSPACE","EMRDELETECOLORSPACE structure [Windows GDI]","EMRSELECTCOLORSPACE","EMRSELECTCOLORSPACE structure [Windows GDI]","EMRSETCOLORSPACE","EMRSETCOLORSPACE structure [Windows GDI]","EMRSETCOLORSPACE","EMRSELECTCOLORSPACE","EMRDELETECOLORSPACE","EMRSETCOLORSPACE","EMRSELECTCOLORSPACE","EMRDELETECOLORSPACE structure [Windows GDI]","PEMRDELETECOLORSPACE","PEMRDELETECOLORSPACE structure pointer [Windows GDI]","PEMRSELECTCOLORSPACE","PEMRSELECTCOLORSPACE structure pointer [Windows GDI]","PEMRSETCOLORSPACE","PEMRSETCOLORSPACE structure pointer [Windows GDI]","_win32_EMRSETCOLORSPACE_str","gdi.emrsetcolorspace__emrselectcolorspace__emrdeletecolorspace","wingdi/EMRDELETECOLORSPACE","wingdi/EMRSELECTCOLORSPACE","wingdi/EMRSETCOLORSPACE","EMRSELECTCOLORSPACE","EMRDELETECOLORSPACE","wingdi/PEMRDELETECOLORSPACE","wingdi/PEMRSELECTCOLORSPACE","wingdi/PEMRSETCOLORSPACE"]
old-location: gdi\emrsetcolorspace__emrselectcolorspace__emrdeletecolorspace.htm
tech.root: gdi
ms.assetid: c661b3cc-6b41-4157-acb4-f9083ab73851
ms.date: 12/05/2018
ms.keywords: '*PEMRDELETECOLORSPACE, *PEMRSELECTCOLORSPACE, *PEMRSETCOLORSPACE, EMRDELETECOLORSPACE, EMRDELETECOLORSPACE structure [Windows GDI], EMRSELECTCOLORSPACE, EMRSELECTCOLORSPACE structure [Windows GDI], EMRSETCOLORSPACE, EMRSETCOLORSPACE structure [Windows GDI], EMRSETCOLORSPACE,EMRSELECTCOLORSPACE,EMRDELETECOLORSPACE, EMRSETCOLORSPACE,EMRSELECTCOLORSPACE,EMRDELETECOLORSPACE structure [Windows GDI], PEMRDELETECOLORSPACE, PEMRDELETECOLORSPACE structure pointer [Windows GDI], PEMRSELECTCOLORSPACE, PEMRSELECTCOLORSPACE structure pointer [Windows GDI], PEMRSETCOLORSPACE, PEMRSETCOLORSPACE structure pointer [Windows GDI], _win32_EMRSETCOLORSPACE_str, gdi.emrsetcolorspace__emrselectcolorspace__emrdeletecolorspace, wingdi/EMRDELETECOLORSPACE, wingdi/EMRSELECTCOLORSPACE, wingdi/EMRSETCOLORSPACE,EMRSELECTCOLORSPACE,EMRDELETECOLORSPACE, wingdi/PEMRDELETECOLORSPACE, wingdi/PEMRSELECTCOLORSPACE, wingdi/PEMRSETCOLORSPACE'
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
req.typenames: EMRSETCOLORSPACE, *PEMRSETCOLORSPACE, EMRSELECTCOLORSPACE, *PEMRSELECTCOLORSPACE, EMRDELETECOLORSPACE, *PEMRDELETECOLORSPACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSETCOLORSPACE
 - wingdi/tagEMRSETCOLORSPACE
 - PEMRSETCOLORSPACE
 - wingdi/PEMRSETCOLORSPACE
 - EMRSETCOLORSPACE
 - wingdi/EMRSETCOLORSPACE
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
 - EMRSETCOLORSPACE
---

# EMRSETCOLORSPACE structure


## -description

The <b>EMRSETCOLORSPACE</b>, <b>EMRSELECTCOLORSPACE</b>, and <b>EMRDELETECOLORSPACE</b> structures contain members for the <b>SetColorSpace</b> and <b>DeleteColorSpace</b> enhanced metafile records.

## -struct-fields

### -field emr

Base structure for all record types.

### -field ihCS

Color space handle index.

## -remarks

There is no function that generates an enhanced metafile record with the <b>EMRSELECTCOLORSPACE</b> structure.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>