---
UID: NS:ddrawint._DD_DESTROYMOCOMPDATA
title: DD_DESTROYMOCOMPDATA (ddrawint.h)
description: The DD_DESTROYMOCOMPDATA structure contains the information required to finish performing motion compensation.
helpviewer_keywords: ["*PDD_DESTROYMOCOMPDATA","DD_DESTROYMOCOMPDATA","DD_DESTROYMOCOMPDATA structure [Display Devices]","ddrawint/DD_DESTROYMOCOMPDATA","ddstrcts_1a3d548c-c0f7-4334-b0c6-b63c155d854c.xml","display.dd_destroymocompdata"]
old-location: display\dd_destroymocompdata.htm
tech.root: display
ms.assetid: 0db32ded-2e32-471d-a752-1f5beffec684
ms.date: 12/05/2018
ms.keywords: '*PDD_DESTROYMOCOMPDATA, DD_DESTROYMOCOMPDATA, DD_DESTROYMOCOMPDATA structure [Display Devices], ddrawint/DD_DESTROYMOCOMPDATA, ddstrcts_1a3d548c-c0f7-4334-b0c6-b63c155d854c.xml, display.dd_destroymocompdata'
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
req.typenames: '*PDD_DESTROYMOCOMPDATA, DD_DESTROYMOCOMPDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_DESTROYMOCOMPDATA
 - ddrawint/_DD_DESTROYMOCOMPDATA
 - PDD_DESTROYMOCOMPDATA
 - ddrawint/PDD_DESTROYMOCOMPDATA
 - DD_DESTROYMOCOMPDATA
 - ddrawint/DD_DESTROYMOCOMPDATA
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
 - DD_DESTROYMOCOMPDATA
---

# DD_DESTROYMOCOMPDATA structure


## -description

The DD_DESTROYMOCOMPDATA structure contains the information required to finish performing motion compensation.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpMoComp

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncomp_local">DD_MOTIONCOMP_LOCAL</a> structure that contains a description of the motion compensation being requested.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_destroy">DdMoCompDestroy</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_destroy">DdMoCompDestroy</a>