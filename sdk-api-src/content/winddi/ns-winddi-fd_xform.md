---
UID: NS:winddi._FD_XFORM
title: FD_XFORM (winddi.h)
description: The FD_XFORM structure describes an arbitrary two-dimensional font transform.
helpviewer_keywords: ["*PFD_XFORM","FD_XFORM","FD_XFORM structure [Display Devices]","PFD_XFORM","PFD_XFORM structure pointer [Display Devices]","display.fd_xform","grstrcts_c68b9048-8da3-4c5d-b977-6bd50cbd6703.xml","winddi/FD_XFORM","winddi/PFD_XFORM"]
old-location: display\fd_xform.htm
tech.root: display
ms.assetid: 4d15a771-fbf2-46ed-9698-faa3840f5f76
ms.date: 12/05/2018
ms.keywords: '*PFD_XFORM, FD_XFORM, FD_XFORM structure [Display Devices], PFD_XFORM, PFD_XFORM structure pointer [Display Devices], display.fd_xform, grstrcts_c68b9048-8da3-4c5d-b977-6bd50cbd6703.xml, winddi/FD_XFORM, winddi/PFD_XFORM'
req.header: winddi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: FD_XFORM, *PFD_XFORM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FD_XFORM
 - winddi/_FD_XFORM
 - PFD_XFORM
 - winddi/PFD_XFORM
 - FD_XFORM
 - winddi/FD_XFORM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - FD_XFORM
---

# FD_XFORM structure


## -description

The FD_XFORM structure describes an arbitrary two-dimensional font transform.

## -struct-fields

### -field eXX

### -field eXY

### -field eYX

### -field eYY

Are the four elements that comprise a 2x2 row-major matrix. <b>eXX</b> and <b>eXY</b> are the elements in the first row; <b>eYX</b> and <b>eYY</b> are the elements in the second row.

## -remarks

This structure is used typically to hold notional-to-device-space font transformations.

