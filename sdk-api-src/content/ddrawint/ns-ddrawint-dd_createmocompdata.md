---
UID: NS:ddrawint._DD_CREATEMOCOMPDATA
title: DD_CREATEMOCOMPDATA (ddrawint.h)
description: The DD_CREATEMOCOMPDATA structure contains the data required to begin using motion compensation.
helpviewer_keywords: ["*PDD_CREATEMOCOMPDATA","DD_CREATEMOCOMPDATA","DD_CREATEMOCOMPDATA structure [Display Devices]","ddrawint/DD_CREATEMOCOMPDATA","ddstrcts_776346bf-3538-4965-b747-a017a7c21514.xml","display.dd_createmocompdata"]
old-location: display\dd_createmocompdata.htm
tech.root: display
ms.assetid: 53b2aa38-b007-4938-8fdb-c3482735ae36
ms.date: 12/05/2018
ms.keywords: '*PDD_CREATEMOCOMPDATA, DD_CREATEMOCOMPDATA, DD_CREATEMOCOMPDATA structure [Display Devices], ddrawint/DD_CREATEMOCOMPDATA, ddstrcts_776346bf-3538-4965-b747-a017a7c21514.xml, display.dd_createmocompdata'
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
req.typenames: '*PDD_CREATEMOCOMPDATA, DD_CREATEMOCOMPDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_CREATEMOCOMPDATA
 - ddrawint/_DD_CREATEMOCOMPDATA
 - PDD_CREATEMOCOMPDATA
 - ddrawint/PDD_CREATEMOCOMPDATA
 - DD_CREATEMOCOMPDATA
 - ddrawint/DD_CREATEMOCOMPDATA
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
 - DD_CREATEMOCOMPDATA
---

# DD_CREATEMOCOMPDATA structure


## -description

The DD_CREATEMOCOMPDATA structure contains the data required to begin using motion compensation.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpMoComp

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncomp_local">DD_MOTIONCOMP_LOCAL</a> structure that contains a description of the motion compensation object.

### -field lpGuid

Points to a GUID that describes the motion compensation process being used.

### -field dwUncompWidth

Specifies the width in pixels of the uncompressed output frame.

### -field dwUncompHeight

Specifies the height in pixels of the uncompressed output frame.

### -field ddUncompPixelFormat

Points to a <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure that contains the format of the uncompressed output frame.

### -field lpData

Points to an optional data buffer that contains any optional information required by the GUID given in <b>lpGuid</b>. This buffer cannot contain any embedded pointers.

### -field dwDataSize

Indicates the size in bytes of the data buffer contained in <b>lpData</b>.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_create">DdMoCompCreate</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_create">DdMoCompCreate</a>