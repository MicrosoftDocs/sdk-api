---
UID: NS:ddrawint._DD_NONLOCALVIDMEMCAPS
title: DD_NONLOCALVIDMEMCAPS (ddrawint.h)
description: The DD_NONLOCALVIDMEMCAPS structure contains the capabilities for nonlocal display memory.
helpviewer_keywords: ["*PDD_NONLOCALVIDMEMCAPS","DD_NONLOCALVIDMEMCAPS","DD_NONLOCALVIDMEMCAPS structure [Display Devices]","PDD_NONLOCALVIDMEMCAPS","PDD_NONLOCALVIDMEMCAPS structure pointer [Display Devices]","ddrawint/DD_NONLOCALVIDMEMCAPS","ddrawint/PDD_NONLOCALVIDMEMCAPS","ddstrcts_2f88c083-47c5-4ae6-a0bc-42d32d6e44c9.xml","display.dd_nonlocalvidmemcaps"]
old-location: display\dd_nonlocalvidmemcaps.htm
tech.root: display
ms.assetid: 1ccc7de7-e5a3-4dc0-9375-a54460d43936
ms.date: 12/05/2018
ms.keywords: '*PDD_NONLOCALVIDMEMCAPS, DD_NONLOCALVIDMEMCAPS, DD_NONLOCALVIDMEMCAPS structure [Display Devices], PDD_NONLOCALVIDMEMCAPS, PDD_NONLOCALVIDMEMCAPS structure pointer [Display Devices], ddrawint/DD_NONLOCALVIDMEMCAPS, ddrawint/PDD_NONLOCALVIDMEMCAPS, ddstrcts_2f88c083-47c5-4ae6-a0bc-42d32d6e44c9.xml, display.dd_nonlocalvidmemcaps'
req.header: ddrawint.h
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
req.typenames: DD_NONLOCALVIDMEMCAPS, *PDD_NONLOCALVIDMEMCAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_NONLOCALVIDMEMCAPS
 - ddrawint/_DD_NONLOCALVIDMEMCAPS
 - PDD_NONLOCALVIDMEMCAPS
 - ddrawint/PDD_NONLOCALVIDMEMCAPS
 - DD_NONLOCALVIDMEMCAPS
 - ddrawint/DD_NONLOCALVIDMEMCAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_NONLOCALVIDMEMCAPS
---

# DD_NONLOCALVIDMEMCAPS structure


## -description

The DD_NONLOCALVIDMEMCAPS structure contains the capabilities for nonlocal display memory.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DD_NONLOCALVIDMEMCAPS structure.

### -field dwNLVBCaps

Contains the driver-specific capabilities for nonlocal-to-local display memory blits. See the Remarks section for more information.

### -field dwNLVBCaps2

Contains more of the driver-specific capabilities for nonlocal-to-local display memory blits. See the Remarks section for more information.

### -field dwNLVBCKeyCaps

Contains driver color key capabilities for nonlocal-to-local display memory blits. See the Remarks section for more information.

### -field dwNLVBFXCaps

Contains driver FX capabilities for nonlocal-to-local display memory blits. See the Remarks section for more information.

### -field dwNLVBRops

Specifies an array of DD_ROP_SPACE DWORDs containing the raster operations supported for nonlocal-to-local blits. The constant DD_ROP_SPACE is defined in <i>ddraw.h</i>. See the Remarks section for more information.

## -remarks

On Microsoft Windows 2000 and later versions, the data structure is called DD_NONLOCALVIDMEMCAPS and on Windows 98/Me the data structure is called DDNONLOCALVIDMEMCAPS.

Normally, the <b>dwNLVBCaps</b>, <b>dwNLVBCaps2</b>, <b>dwNFLBCKeyCaps</b>, <b>dwNLVBFXCaps</b>, and <b>dwNLVBRops</b> members contain a subset of the flags used in the <a href="/windows/desktop/api/ddrawi/ns-ddrawi-ddcorecaps">DDCORECAPS</a> structure that is relevant to nonlocal-to-local blitting. However, to allow flexibility for device driver writers, any of the flags in DDCORECAPS can be used.

## -see-also

<a href="/windows/desktop/api/ddrawi/ns-ddrawi-ddcorecaps">DDCORECAPS</a>