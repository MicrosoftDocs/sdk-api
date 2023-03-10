---
UID: NS:ddrawint.DD_NTPRIVATEDRIVERCAPS
title: DD_NTPRIVATEDRIVERCAPS (ddrawint.h)
description: The DD_NTPRIVATEDRIVERCAPS structure enables the driver to change the behavior of Microsoft DirectDraw when DirectDraw is creating surfaces.
helpviewer_keywords: ["DD_NTPRIVATEDRIVERCAPS","DD_NTPRIVATEDRIVERCAPS structure [Display Devices]","ddrawint/DD_NTPRIVATEDRIVERCAPS","ddstrcts_37e03d8c-1dc6-44d4-afe7-1f92acb58898.xml","display.dd_ntprivatedrivercaps"]
old-location: display\dd_ntprivatedrivercaps.htm
tech.root: display
ms.assetid: d802b080-cf94-400a-96c4-e765008dfc8a
ms.date: 12/05/2018
ms.keywords: DD_NTPRIVATEDRIVERCAPS, DD_NTPRIVATEDRIVERCAPS structure [Display Devices], ddrawint/DD_NTPRIVATEDRIVERCAPS, ddstrcts_37e03d8c-1dc6-44d4-afe7-1f92acb58898.xml, display.dd_ntprivatedrivercaps
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
req.typenames: DD_NTPRIVATEDRIVERCAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DD_NTPRIVATEDRIVERCAPS
 - ddrawint/DD_NTPRIVATEDRIVERCAPS
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
 - DD_NTPRIVATEDRIVERCAPS
---

# DD_NTPRIVATEDRIVERCAPS structure


## -description

The DD_NTPRIVATEDRIVERCAPS structure enables the driver to change the behavior of Microsoft DirectDraw when DirectDraw is creating surfaces.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DD_NTPRIVATEDRIVERCAPS structure.

### -field dwPrivateCaps

Indicates how DirectDraw should create the surface.





#### DDHAL_PRIVATECAP_AUTOMICSURFACECREATION

When this flag is set, it indicates that the driver requests <a href="/previous-versions/windows/hardware/drivers/ff549263(v=vs.85)">DdCreateSurface</a> to be called only once when the application creates a complex flipping chain using a single <b>CreateSurface</b> call. In this case, the <b>lplpSList</b> member of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_createsurfacedata">DD_CREATESURFACEDATA</a> structure points to a list of surfaces to create (rather than a single surface) and <b>dwSCnt</b> contains the number of surfaces in the list. 



#### DDHAL_PRIVATECAP_NOTIFYPRIMARYCREATION

When this flag is set, the driver's <a href="/previous-versions/windows/hardware/drivers/ff549263(v=vs.85)">DdCreateSurface</a> function is called when creating a primary surface. If this flag is not set, the driver's <i>DdCreateSurface</i> function is not called.

## -remarks

The behavior of DirectDraw emulates the surface creation techniques employed by DirectDraw when creating surfaces for Microsoft Windows 98/Me.

When the DDHAL_PRIVATECAP_AUTOMICSURFACECREATION flag is not set, DirectDraw performs surface creation using the original method, that is, it calls the driver's <a href="/previous-versions/windows/hardware/drivers/ff549263(v=vs.85)">DdCreateSurface</a> function once for each surface being created.

When the DDHAL_PRIVATECAP_NOTIFYPRIMARYCREATION flag is not set, DirectDraw performs primary surface creation using the original method, that is, it does not call the driver when creating a primary surface.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_createsurfacedata">DD_CREATESURFACEDATA</a>



<a href="/previous-versions/windows/hardware/drivers/ff549263(v=vs.85)">DdCreateSurface</a>