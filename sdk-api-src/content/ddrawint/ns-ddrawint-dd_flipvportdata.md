---
UID: NS:ddrawint._DD_FLIPVPORTDATA
title: DD_FLIPVPORTDATA (ddrawint.h)
description: The DD_FLIPVPORTDATA structure contains the information necessary for the video port extensions (VPE) object to perform a flip.
helpviewer_keywords: ["*PDD_FLIPVPORTDATA","DD_FLIPVPORTDATA","DD_FLIPVPORTDATA structure [Display Devices]","ddrawint/DD_FLIPVPORTDATA","ddstrcts_9af598a7-a7fc-40f2-a1dd-355964f60da9.xml","display.dd_flipvportdata"]
old-location: display\dd_flipvportdata.htm
tech.root: display
ms.assetid: 1bc6dc12-1213-47d7-9e6f-2396a41cc6d0
ms.date: 12/05/2018
ms.keywords: '*PDD_FLIPVPORTDATA, DD_FLIPVPORTDATA, DD_FLIPVPORTDATA structure [Display Devices], ddrawint/DD_FLIPVPORTDATA, ddstrcts_9af598a7-a7fc-40f2-a1dd-355964f60da9.xml, display.dd_flipvportdata'
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
req.typenames: '*PDD_FLIPVPORTDATA, DD_FLIPVPORTDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_FLIPVPORTDATA
 - ddrawint/_DD_FLIPVPORTDATA
 - PDD_FLIPVPORTDATA
 - ddrawint/PDD_FLIPVPORTDATA
 - DD_FLIPVPORTDATA
 - ddrawint/DD_FLIPVPORTDATA
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
 - DD_FLIPVPORTDATA
---

# DD_FLIPVPORTDATA structure


## -description

The DD_FLIPVPORTDATA structure contains the information necessary for the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object to perform a flip.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpVideoPort

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure that represents this VPE object.

### -field lpSurfCurr

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure for the current surface; that is, the surface on which data is currently being written.

### -field lpSurfTarg

Points to a DD_SURFACE_LOCAL structure for the target surface; that is, the surface to which the driver should flip.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_flip">DdVideoPortFlip</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field FlipVideoPort

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_flip">DdVideoPortFlip</a>