---
UID: NS:winddi._XFORMOBJ
title: XFORMOBJ
description: The XFORMOBJ structure describes an arbitrary linear two-dimensional transform, such as for geometric wide lines.
ms.date: 07/12/2022
tech.root: display
helpviewer_keywords:
 - _XFORMOBJ
req.construct-type: structure
req.header: winddi.h
req.include-header: Winddi.h
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
req.typenames: XFORMOBJ
req.redist: 
f1_keywords:
 - _XFORMOBJ
 - winddi/_XFORMOBJ
 - XFORMOBJ
 - winddi/XFORMOBJ
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
 - _XFORMOBJ
 - XFORMOBJ
---

## -description

The XFORMOBJ structure describes an arbitrary linear two-dimensional transform, such as for geometric wide lines.

## -struct-fields

### -field ulReserved

There are no public members in the XFORMOBJ structure.

## -remarks

The arbitrary two-dimensional transform can be downloaded to the driver. Functions are also provided to apply the transform to driver-supplied data.

## -see-also

* [FONTOBJ_pxoGetXform](/windows/win32/api/winddi/nf-winddi-fontobj_pxogetxform)
* [XFORMOBJ_bApplyXform](/windows/win32/api/winddi/nf-winddi-xformobj_bapplyxform)
* [XFORMOBJ_iGetXform](/windows/win32/api/winddi/nf-winddi-xformobj_igetxform)
