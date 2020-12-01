---
UID: NS:wingdi.tagEMRSETWORLDTRANSFORM
title: EMRSETWORLDTRANSFORM (wingdi.h)
description: The EMRSETWORLDTRANSFORM structure contains members for the SetWorldTransform enhanced metafile record.
helpviewer_keywords: ["*PEMRSETWORLDTRANSFORM","EMRSETWORLDTRANSFORM","EMRSETWORLDTRANSFORM structure [Windows GDI]","PEMRSETWORLDTRANSFORM","PEMRSETWORLDTRANSFORM structure pointer [Windows GDI]","_win32_EMRSETWORLDTRANSFORM_str","gdi.emrsetworldtransform","wingdi/EMRSETWORLDTRANSFORM","wingdi/PEMRSETWORLDTRANSFORM"]
old-location: gdi\emrsetworldtransform.htm
tech.root: gdi
ms.assetid: 08e5e272-22b5-4097-a293-f5a1fd865edf
ms.date: 12/05/2018
ms.keywords: '*PEMRSETWORLDTRANSFORM, EMRSETWORLDTRANSFORM, EMRSETWORLDTRANSFORM structure [Windows GDI], PEMRSETWORLDTRANSFORM, PEMRSETWORLDTRANSFORM structure pointer [Windows GDI], _win32_EMRSETWORLDTRANSFORM_str, gdi.emrsetworldtransform, wingdi/EMRSETWORLDTRANSFORM, wingdi/PEMRSETWORLDTRANSFORM'
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
req.typenames: EMRSETWORLDTRANSFORM, *PEMRSETWORLDTRANSFORM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSETWORLDTRANSFORM
 - wingdi/tagEMRSETWORLDTRANSFORM
 - PEMRSETWORLDTRANSFORM
 - wingdi/PEMRSETWORLDTRANSFORM
 - EMRSETWORLDTRANSFORM
 - wingdi/EMRSETWORLDTRANSFORM
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
 - EMRSETWORLDTRANSFORM
---

# EMRSETWORLDTRANSFORM structure


## -description

The <b>EMRSETWORLDTRANSFORM</b> structure contains members for the <b>SetWorldTransform</b> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field xform

World-space to page-space transformation data.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setworldtransform">SetWorldTransform</a>