---
UID: NS:ddrawint._DD_QUERYMOCOMPSTATUSDATA
title: DD_QUERYMOCOMPSTATUSDATA (ddrawint.h)
description: The DD_QUERYMOCOMPSTATUSDATA structure contains information required to query the status of the previous frame.
helpviewer_keywords: ["*PDD_QUERYMOCOMPSTATUSDATA","DD_QUERYMOCOMPSTATUSDATA","DD_QUERYMOCOMPSTATUSDATA structure [Display Devices]","ddrawint/DD_QUERYMOCOMPSTATUSDATA","ddstrcts_d8a10a3c-886c-4cef-b4a0-2db5f4c45927.xml","display.dd_querymocompstatusdata"]
old-location: display\dd_querymocompstatusdata.htm
tech.root: display
ms.assetid: 53e2c8c7-dc6b-4c0b-9555-9aac07bd9186
ms.date: 12/05/2018
ms.keywords: '*PDD_QUERYMOCOMPSTATUSDATA, DD_QUERYMOCOMPSTATUSDATA, DD_QUERYMOCOMPSTATUSDATA structure [Display Devices], ddrawint/DD_QUERYMOCOMPSTATUSDATA, ddstrcts_d8a10a3c-886c-4cef-b4a0-2db5f4c45927.xml, display.dd_querymocompstatusdata'
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
req.typenames: '*PDD_QUERYMOCOMPSTATUSDATA, DD_QUERYMOCOMPSTATUSDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_QUERYMOCOMPSTATUSDATA
 - ddrawint/_DD_QUERYMOCOMPSTATUSDATA
 - PDD_QUERYMOCOMPSTATUSDATA
 - ddrawint/PDD_QUERYMOCOMPSTATUSDATA
 - DD_QUERYMOCOMPSTATUSDATA
 - ddrawint/DD_QUERYMOCOMPSTATUSDATA
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
 - DD_QUERYMOCOMPSTATUSDATA
---

# DD_QUERYMOCOMPSTATUSDATA structure


## -description

The DD_QUERYMOCOMPSTATUSDATA structure contains information required to query the status of the previous frame.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpMoComp

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncomp_local">DD_MOTIONCOMP_LOCAL</a> structure that contains a description of the motion compensation being requested.

### -field lpSurface

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that contains the surface being queried.

### -field dwFlags

Indicates the type of surface access.





#### DDMCQUERY_READ

Indicates that the surface can only be tested for read or display access. If this flag is not set, the surface can be tested for write access.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_querystatus">DdMoCompQueryStatus</a> callback. A return code of DD_OK indicates the hardware has finished processing the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_render">DdMoCompRender</a> request. Otherwise the return value must be DDERR_WASSTILLDRAWING. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_querystatus">DdMoCompQueryStatus</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_render">DdMoCompRender</a>