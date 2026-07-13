---
UID: NS:wingdi.tagEMRFILLPATH
title: EMRFILLPATH (wingdi.h)
description: The EMRFILLPATH, EMRSTROKEANDFILLPATH, and EMRSTROKEPATH structures contain members for the FillPath, StrokeAndFillPath, and StrokePath enhanced metafile records.
helpviewer_keywords: ["*PEMRFILLPATH","*PEMRSTROKEANDFILLPATH","*PEMRSTROKEPATH","EMRFILLPATH","EMRFILLPATH structure [Windows GDI]","EMRFILLPATH","EMRSTROKEANDFILLPATH","EMRSTROKEPATH","EMRFILLPATH","EMRSTROKEANDFILLPATH","EMRSTROKEPATH structure [Windows GDI]","EMRSTROKEANDFILLPATH","EMRSTROKEANDFILLPATH structure [Windows GDI]","EMRSTROKEPATH","EMRSTROKEPATH structure [Windows GDI]","PEMRFILLPATH","PEMRFILLPATH structure pointer [Windows GDI]","PEMRSTROKEANDFILLPATH","PEMRSTROKEANDFILLPATH structure pointer [Windows GDI]","PEMRSTROKEPATH","PEMRSTROKEPATH structure pointer [Windows GDI]","_win32_EMRFILLPATH_str","gdi.emrfillpath__emrstrokeandfillpath__emrstrokepath","wingdi/EMRFILLPATH","EMRSTROKEANDFILLPATH","EMRSTROKEPATH","wingdi/EMRSTROKEANDFILLPATH","wingdi/EMRSTROKEPATH","wingdi/PEMRFILLPATH","wingdi/PEMRSTROKEANDFILLPATH","wingdi/PEMRSTROKEPATH"]
old-location: gdi\emrfillpath__emrstrokeandfillpath__emrstrokepath.htm
tech.root: gdi
ms.assetid: 9911e0fb-2e0d-4684-bff6-fc876ab8185d
ms.date: 12/05/2018
ms.keywords: '*PEMRFILLPATH, *PEMRSTROKEANDFILLPATH, *PEMRSTROKEPATH, EMRFILLPATH, EMRFILLPATH structure [Windows GDI], EMRFILLPATH,EMRSTROKEANDFILLPATH,EMRSTROKEPATH, EMRFILLPATH,EMRSTROKEANDFILLPATH,EMRSTROKEPATH structure [Windows GDI], EMRSTROKEANDFILLPATH, EMRSTROKEANDFILLPATH structure [Windows GDI], EMRSTROKEPATH, EMRSTROKEPATH structure [Windows GDI], PEMRFILLPATH, PEMRFILLPATH structure pointer [Windows GDI], PEMRSTROKEANDFILLPATH, PEMRSTROKEANDFILLPATH structure pointer [Windows GDI], PEMRSTROKEPATH, PEMRSTROKEPATH structure pointer [Windows GDI], _win32_EMRFILLPATH_str, gdi.emrfillpath__emrstrokeandfillpath__emrstrokepath, wingdi/EMRFILLPATH,EMRSTROKEANDFILLPATH,EMRSTROKEPATH, wingdi/EMRSTROKEANDFILLPATH, wingdi/EMRSTROKEPATH, wingdi/PEMRFILLPATH, wingdi/PEMRSTROKEANDFILLPATH, wingdi/PEMRSTROKEPATH'
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
req.typenames: EMRFILLPATH, *PEMRFILLPATH, EMRSTROKEANDFILLPATH, *PEMRSTROKEANDFILLPATH, EMRSTROKEPATH, *PEMRSTROKEPATH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRFILLPATH
 - wingdi/tagEMRFILLPATH
 - PEMRFILLPATH
 - wingdi/PEMRFILLPATH
 - EMRFILLPATH
 - wingdi/EMRFILLPATH
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
 - EMRFILLPATH
---

# EMRFILLPATH structure


## -description

The <b>EMRFILLPATH</b>, <b>EMRSTROKEANDFILLPATH</b>,  and <b>EMRSTROKEPATH</b> structures contain members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-fillpath">FillPath</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-strokeandfillpath">StrokeAndFillPath</a>, and <a href="/windows/desktop/api/wingdi/nf-wingdi-strokepath">StrokePath</a> enhanced metafile records.

## -struct-fields

### -field emr

Base structure for all record types.

### -field rclBounds

Bounding rectangle, in device units.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>