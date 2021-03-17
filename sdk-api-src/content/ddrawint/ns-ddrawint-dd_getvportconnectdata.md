---
UID: NS:ddrawint._DD_GETVPORTCONNECTDATA
title: DD_GETVPORTCONNECTDATA (ddrawint.h)
description: The DD_GETVPORTCONNECTDATA structure contains the connection combinations supported by the specified video port extensions (VPE) object.
helpviewer_keywords: ["*PDD_GETVPORTCONNECTDATA","DD_GETVPORTCONNECTDATA","DD_GETVPORTCONNECTDATA structure [Display Devices]","ddrawint/DD_GETVPORTCONNECTDATA","ddstrcts_56b2c83f-8798-4960-8fb6-062ccd1d5dd3.xml","display.dd_getvportconnectdata"]
old-location: display\dd_getvportconnectdata.htm
tech.root: display
ms.assetid: 74cea50f-b8fd-4c32-815f-19f075b74838
ms.date: 12/05/2018
ms.keywords: '*PDD_GETVPORTCONNECTDATA, DD_GETVPORTCONNECTDATA, DD_GETVPORTCONNECTDATA structure [Display Devices], ddrawint/DD_GETVPORTCONNECTDATA, ddstrcts_56b2c83f-8798-4960-8fb6-062ccd1d5dd3.xml, display.dd_getvportconnectdata'
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
req.typenames: '*PDD_GETVPORTCONNECTDATA, DD_GETVPORTCONNECTDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETVPORTCONNECTDATA
 - ddrawint/_DD_GETVPORTCONNECTDATA
 - PDD_GETVPORTCONNECTDATA
 - ddrawint/PDD_GETVPORTCONNECTDATA
 - DD_GETVPORTCONNECTDATA
 - ddrawint/DD_GETVPORTCONNECTDATA
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
 - DD_GETVPORTCONNECTDATA
---

# DD_GETVPORTCONNECTDATA structure


## -description

The DD_GETVPORTCONNECTDATA structure contains the connection combinations supported by the specified <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.

### -field dwPortId

Specifies the ID of the VPE object for which the driver is to retrieve connection information. DirectDraw obtains this ID from the <b>dwVideoPortID</b> member of the <a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportcaps">DDVIDEOPORTCAPS</a> structure.

### -field lpConnect

Points to an array of <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddvideoportconnect">DDVIDEOPORTCONNECT</a> structures in which the driver should return the characteristics of each connection that the VPE object supports. This member can be <b>NULL</b>.

### -field dwNumEntries

Specifies the location in which the driver returns the number of connection combinations supported by the specified VPE object.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getvportconnect">DdVideoPortGetConnectInfo</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field GetVideoPortConnectInfo

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportcaps">DDVIDEOPORTCAPS</a>



<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddvideoportconnect">DDVIDEOPORTCONNECT</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getvportconnect">DdVideoPortGetConnectInfo</a>