---
UID: NS:ddrawint._DD_GETINTERNALMOCOMPDATA
title: DD_GETINTERNALMOCOMPDATA (ddrawint.h)
description: The DD_GETINTERNALMOCOMPDATA structure contains the internal memory requirements.
helpviewer_keywords: ["*PDD_GETINTERNALMOCOMPDATA","DD_GETINTERNALMOCOMPDATA","DD_GETINTERNALMOCOMPDATA structure [Display Devices]","ddrawint/DD_GETINTERNALMOCOMPDATA","ddstrcts_02721b17-cf19-462c-b588-039431b8d548.xml","display.dd_getinternalmocompdata"]
old-location: display\dd_getinternalmocompdata.htm
tech.root: display
ms.assetid: 5d8f722f-7574-485e-9ff2-568cd0ae23f7
ms.date: 12/05/2018
ms.keywords: '*PDD_GETINTERNALMOCOMPDATA, DD_GETINTERNALMOCOMPDATA, DD_GETINTERNALMOCOMPDATA structure [Display Devices], ddrawint/DD_GETINTERNALMOCOMPDATA, ddstrcts_02721b17-cf19-462c-b588-039431b8d548.xml, display.dd_getinternalmocompdata'
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
req.typenames: '*PDD_GETINTERNALMOCOMPDATA, DD_GETINTERNALMOCOMPDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETINTERNALMOCOMPDATA
 - ddrawint/_DD_GETINTERNALMOCOMPDATA
 - PDD_GETINTERNALMOCOMPDATA
 - ddrawint/PDD_GETINTERNALMOCOMPDATA
 - DD_GETINTERNALMOCOMPDATA
 - ddrawint/DD_GETINTERNALMOCOMPDATA
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
 - DD_GETINTERNALMOCOMPDATA
---

# DD_GETINTERNALMOCOMPDATA structure


## -description

The DD_GETINTERNALMOCOMPDATA structure contains the internal memory requirements.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpGuid

Points to a GUID for which the internal memory requirement is requested.

### -field dwWidth

Indicates the width in pixels of uncompressed output frame.

### -field dwHeight

Indicates the height in pixels of uncompressed output frame.

### -field ddPixelFormat

Points to a <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure that contains the pixel format of the uncompressed output frame.

### -field dwScratchMemAlloc

Indicates the size in bytes of internal memory that the display driver privately reserves to perform motion compensation

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getinternalinfo">DdMoCompGetInternalInfo</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getinternalinfo">DdMoCompGetInternalInfo</a>