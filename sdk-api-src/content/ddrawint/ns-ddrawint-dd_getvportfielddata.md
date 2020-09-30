---
UID: NS:ddrawint._DD_GETVPORTFIELDDATA
title: DD_GETVPORTFIELDDATA (ddrawint.h)
description: The DD_GETVPORTFIELDDATA structure contains the information required for the driver to determine whether the current field of an interlaced signal is even or odd.
helpviewer_keywords: ["*PDD_GETVPORTFIELDDATA","DD_GETVPORTFIELDDATA","DD_GETVPORTFIELDDATA structure [Display Devices]","ddrawint/DD_GETVPORTFIELDDATA","ddstrcts_777ca41f-3364-4f07-96cb-cd249ff16179.xml","display.dd_getvportfielddata"]
old-location: display\dd_getvportfielddata.htm
tech.root: display
ms.assetid: 549956f8-c39f-4cc3-b72a-b1e3785463e8
ms.date: 12/05/2018
ms.keywords: '*PDD_GETVPORTFIELDDATA, DD_GETVPORTFIELDDATA, DD_GETVPORTFIELDDATA structure [Display Devices], ddrawint/DD_GETVPORTFIELDDATA, ddstrcts_777ca41f-3364-4f07-96cb-cd249ff16179.xml, display.dd_getvportfielddata'
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
req.typenames: '*PDD_GETVPORTFIELDDATA, DD_GETVPORTFIELDDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETVPORTFIELDDATA
 - ddrawint/_DD_GETVPORTFIELDDATA
 - PDD_GETVPORTFIELDDATA
 - ddrawint/PDD_GETVPORTFIELDDATA
 - DD_GETVPORTFIELDDATA
 - ddrawint/DD_GETVPORTFIELDDATA
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
 - DD_GETVPORTFIELDDATA
---

# DD_GETVPORTFIELDDATA structure


## -description

The DD_GETVPORTFIELDDATA structure contains the information required for the driver to determine whether the current field of an interlaced signal is even or odd.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field lpVideoPort

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure that represents this <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object.

### -field bField

Specifies the location in which the driver should indicate the polarity of the field. This member should be set to <b>TRUE</b> if the current field is the even field of an interlaced signal and to <b>FALSE</b> if the current field is the odd field.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getfield">DdVideoPortGetField</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field GetVideoPortField

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getfield">DdVideoPortGetField</a>