---
UID: NS:ddrawint._DD_GETMOCOMPFORMATSDATA
title: DD_GETMOCOMPFORMATSDATA (ddrawint.h)
description: The DD_GETMOCOMPFORMATSDATA structure contains the uncompressed format information.
helpviewer_keywords: ["*PDD_GETMOCOMPFORMATSDATA","DD_GETMOCOMPFORMATSDATA","DD_GETMOCOMPFORMATSDATA structure [Display Devices]","ddrawint/DD_GETMOCOMPFORMATSDATA","ddstrcts_641a377d-109e-43f2-bc12-631964737386.xml","display.dd_getmocompformatsdata"]
old-location: display\dd_getmocompformatsdata.htm
tech.root: display
ms.assetid: 1effebea-1cdb-46e9-a783-5a68863a2756
ms.date: 12/05/2018
ms.keywords: '*PDD_GETMOCOMPFORMATSDATA, DD_GETMOCOMPFORMATSDATA, DD_GETMOCOMPFORMATSDATA structure [Display Devices], ddrawint/DD_GETMOCOMPFORMATSDATA, ddstrcts_641a377d-109e-43f2-bc12-631964737386.xml, display.dd_getmocompformatsdata'
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
req.typenames: '*PDD_GETMOCOMPFORMATSDATA, DD_GETMOCOMPFORMATSDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETMOCOMPFORMATSDATA
 - ddrawint/_DD_GETMOCOMPFORMATSDATA
 - PDD_GETMOCOMPFORMATSDATA
 - ddrawint/PDD_GETMOCOMPFORMATSDATA
 - DD_GETMOCOMPFORMATSDATA
 - ddrawint/DD_GETMOCOMPFORMATSDATA
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
 - DD_GETMOCOMPFORMATSDATA
---

# DD_GETMOCOMPFORMATSDATA structure


## -description

The DD_GETMOCOMPFORMATSDATA structure contains the uncompressed format information.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpGuid

Points to a GUID that describes the uncompressed formats being requested.

### -field dwNumFormats

Indicates the number of uncompressed formats supported for the specified GUID.

### -field lpFormats

Points to a <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure that contains the motion compensation pixel format. If this member is not <b>NULL</b>, the uncompressed formats are copied into the buffer pointed to by this member.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getformats">DdMoCompGetFormats</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mocompcb_getformats">DdMoCompGetFormats</a>