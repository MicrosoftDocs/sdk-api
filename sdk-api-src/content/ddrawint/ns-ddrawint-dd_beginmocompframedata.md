---
UID: NS:ddrawint._DD_BEGINMOCOMPFRAMEDATA
title: DD_BEGINMOCOMPFRAMEDATA (ddrawint.h)
description: The DDHAL_BEGINMOCOMPFRAMEDATA structure contains the frame information required to start decoding.
helpviewer_keywords: ["*PDD_BEGINMOCOMPFRAMEDATA","DD_BEGINMOCOMPFRAMEDATA","DD_BEGINMOCOMPFRAMEDATA structure [Display Devices]","ddrawint/DD_BEGINMOCOMPFRAMEDATA","ddstrcts_6e61d707-7245-4d0d-aaa5-f63bb610d2e5.xml","display.dd_beginmocompframedata"]
old-location: display\dd_beginmocompframedata.htm
tech.root: display
ms.assetid: 4a75642d-87e3-4c95-be67-2d494bf6122e
ms.date: 12/05/2018
ms.keywords: '*PDD_BEGINMOCOMPFRAMEDATA, DD_BEGINMOCOMPFRAMEDATA, DD_BEGINMOCOMPFRAMEDATA structure [Display Devices], ddrawint/DD_BEGINMOCOMPFRAMEDATA, ddstrcts_6e61d707-7245-4d0d-aaa5-f63bb610d2e5.xml, display.dd_beginmocompframedata'
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
req.typenames: '*PDD_BEGINMOCOMPFRAMEDATA, DD_BEGINMOCOMPFRAMEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_BEGINMOCOMPFRAMEDATA
 - ddrawint/_DD_BEGINMOCOMPFRAMEDATA
 - PDD_BEGINMOCOMPFRAMEDATA
 - ddrawint/PDD_BEGINMOCOMPFRAMEDATA
 - DD_BEGINMOCOMPFRAMEDATA
 - ddrawint/DD_BEGINMOCOMPFRAMEDATA
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
 - DD_BEGINMOCOMPFRAMEDATA
---

# DD_BEGINMOCOMPFRAMEDATA structure


## -description

The DDHAL_BEGINMOCOMPFRAMEDATA structure contains the frame information required to start decoding.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpMoComp

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncomp_local">DD_MOTIONCOMP_LOCAL</a> structure that contains a description of the motion compensation being requested.

### -field lpDestSurface

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure representing the destination surface in which to decode this frame.

### -field dwInputDataSize

Indicates the size in bytes of optional input data in <b>lpInputData</b> that is required to begin this frame.

### -field lpInputData

Points to an optional input buffer, the contents of which are defined by the GUID. This buffer cannot contain any embedded pointers.

### -field dwOutputDataSize

Indicates the size in bytes of optional output data in <b>lpOutputData</b> that is required to begin this frame.

### -field lpOutputData

Points to an optional output buffer, the contents of which are defined by the GUID. This buffer cannot contain any embedded pointers.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_beginframe">DdMoCompBeginFrame</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_beginframe">DdMoCompBeginFrame</a>