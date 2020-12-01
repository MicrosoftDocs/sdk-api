---
UID: NS:wingdi.tagEMRMODIFYWORLDTRANSFORM
title: EMRMODIFYWORLDTRANSFORM (wingdi.h)
description: The EMRMODIFYWORLDTRANSFORM structure contains members for the ModifyWorldTransform enhanced metafile record.
helpviewer_keywords: ["*PEMRMODIFYWORLDTRANSFORM","EMRMODIFYWORLDTRANSFORM","EMRMODIFYWORLDTRANSFORM structure [Windows GDI]","PEMRMODIFYWORLDTRANSFORM","PEMRMODIFYWORLDTRANSFORM structure pointer [Windows GDI]","_win32_EMRMODIFYWORLDTRANSFORM_str","gdi.emrmodifyworldtransform","wingdi/EMRMODIFYWORLDTRANSFORM","wingdi/PEMRMODIFYWORLDTRANSFORM"]
old-location: gdi\emrmodifyworldtransform.htm
tech.root: gdi
ms.assetid: 61d51fc9-a8dd-4981-940d-eedc8936360a
ms.date: 12/05/2018
ms.keywords: '*PEMRMODIFYWORLDTRANSFORM, EMRMODIFYWORLDTRANSFORM, EMRMODIFYWORLDTRANSFORM structure [Windows GDI], PEMRMODIFYWORLDTRANSFORM, PEMRMODIFYWORLDTRANSFORM structure pointer [Windows GDI], _win32_EMRMODIFYWORLDTRANSFORM_str, gdi.emrmodifyworldtransform, wingdi/EMRMODIFYWORLDTRANSFORM, wingdi/PEMRMODIFYWORLDTRANSFORM'
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
req.typenames: EMRMODIFYWORLDTRANSFORM, *PEMRMODIFYWORLDTRANSFORM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRMODIFYWORLDTRANSFORM
 - wingdi/tagEMRMODIFYWORLDTRANSFORM
 - PEMRMODIFYWORLDTRANSFORM
 - wingdi/PEMRMODIFYWORLDTRANSFORM
 - EMRMODIFYWORLDTRANSFORM
 - wingdi/EMRMODIFYWORLDTRANSFORM
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
 - EMRMODIFYWORLDTRANSFORM
---

# EMRMODIFYWORLDTRANSFORM structure


## -description

The <b>EMRMODIFYWORLDTRANSFORM</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-modifyworldtransform">ModifyWorldTransform</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field xform

The world-space to page-space transform data.

### -field iMode

Indicates how the transformation data modifies the current world transformation. This member can be one of the following values: MWT_IDENTITY, MWT_LEFTMULTIPLY, or MWT_RIGHTMULTIPLY.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-emr">EMR</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-modifyworldtransform">ModifyWorldTransform</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a>