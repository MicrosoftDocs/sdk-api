---
UID: NS:magnification.tagMAGTRANSFORM
title: MAGTRANSFORM (magnification.h)
description: Describes a transformation matrix that a magnifier control uses to magnify screen content.
helpviewer_keywords: ["*PMAGTRANSFORM","MAGTRANSFORM","MAGTRANSFORM structure [Magnification API]","PMAGTRANSFORM","PMAGTRANSFORM structure pointer [Magnification API]","magapi.magapi_magtransform","magapi_magtransform","magnification/MAGTRANSFORM","magnification/PMAGTRANSFORM"]
old-location: magapi\magapi_magtransform.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\structures\magtransformstruct.htm
ms.date: 12/05/2018
ms.keywords: '*PMAGTRANSFORM, MAGTRANSFORM, MAGTRANSFORM structure [Magnification API], PMAGTRANSFORM, PMAGTRANSFORM structure pointer [Magnification API], magapi.magapi_magtransform, magapi_magtransform, magnification/MAGTRANSFORM, magnification/PMAGTRANSFORM'
req.header: magnification.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MAGTRANSFORM, *PMAGTRANSFORM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMAGTRANSFORM
 - magnification/tagMAGTRANSFORM
 - PMAGTRANSFORM
 - magnification/PMAGTRANSFORM
 - MAGTRANSFORM
 - magnification/MAGTRANSFORM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Magnification.h
api_name:
 - MAGTRANSFORM
---

# MAGTRANSFORM structure


## -description

Describes a transformation matrix that a magnifier control uses to magnify screen content.

## -struct-fields

### -field v

Type: <b>float[3]</b>

The transformation matrix.

## -remarks

The transformation matrix is 

 (<i>n</i>, 0.0, 0.0)

 (0.0, <i>n</i>, 0.0)

 (0.0, 0.0, 1.0) 

where <i>n</i> is the magnification factor.

## -see-also

<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-maggetwindowtransform">MagGetWindowTransform</a>



<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-magsetwindowtransform">MagSetWindowTransform</a>



<b>Reference</b>