---
UID: NS:ddrawint._DD_SETEXCLUSIVEMODEDATA
title: DD_SETEXCLUSIVEMODEDATA (ddrawint.h)
description: The DD_SETEXCLUSIVEMODEDATA structure contains the exclusive mode notification information.
helpviewer_keywords: ["*PDD_SETEXCLUSIVEMODEDATA","DD_SETEXCLUSIVEMODEDATA","DD_SETEXCLUSIVEMODEDATA structure [Display Devices]","ddrawint/DD_SETEXCLUSIVEMODEDATA","ddstrcts_c6ba3e13-afcd-4e8a-994b-d3c006d2c952.xml","display.dd_setexclusivemodedata"]
old-location: display\dd_setexclusivemodedata.htm
tech.root: display
ms.assetid: b2f5af15-c773-4741-a8dc-71d2b89776a7
ms.date: 12/05/2018
ms.keywords: '*PDD_SETEXCLUSIVEMODEDATA, DD_SETEXCLUSIVEMODEDATA, DD_SETEXCLUSIVEMODEDATA structure [Display Devices], ddrawint/DD_SETEXCLUSIVEMODEDATA, ddstrcts_c6ba3e13-afcd-4e8a-994b-d3c006d2c952.xml, display.dd_setexclusivemodedata'
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
req.typenames: '*PDD_SETEXCLUSIVEMODEDATA, DD_SETEXCLUSIVEMODEDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_SETEXCLUSIVEMODEDATA
 - ddrawint/_DD_SETEXCLUSIVEMODEDATA
 - PDD_SETEXCLUSIVEMODEDATA
 - ddrawint/PDD_SETEXCLUSIVEMODEDATA
 - DD_SETEXCLUSIVEMODEDATA
 - ddrawint/DD_SETEXCLUSIVEMODEDATA
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
 - DD_SETEXCLUSIVEMODEDATA
---

# DD_SETEXCLUSIVEMODEDATA structure


## -description

The DD_SETEXCLUSIVEMODEDATA structure contains the exclusive mode notification information.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field dwEnterExcl

Indicates that a Microsoft DirectDraw application is switching into exclusive mode when <b>TRUE</b>; indicates that a DirectDraw application is leaving exclusive mode when <b>FALSE</b>.

### -field dwReserved

This is reserved for system use and should be ignored by the driver.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_setexclusivemode">DdSetExclusiveMode</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field SetExclusiveMode

Used by the DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_setexclusivemode">DdSetExclusiveMode</a>