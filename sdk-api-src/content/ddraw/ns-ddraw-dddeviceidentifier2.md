---
UID: NS:ddraw.tagDDDEVICEIDENTIFIER2
title: DDDEVICEIDENTIFIER2 (ddraw.h)
description: The DDDEVICEIDENTIFIER2 structure is passed to the IDirectDraw7::GetDeviceIdentifier method to obtain information about a device.
helpviewer_keywords: ["*LPDDDEVICEIDENTIFIER2","DDDEVICEIDENTIFIER2","DDDEVICEIDENTIFIER2 structure [DirectDraw]","LPDDDEVICEIDENTIFIER2","LPDDDEVICEIDENTIFIER2 structure pointer [DirectDraw]","ddraw/DDDEVICEIDENTIFIER2","ddraw/LPDDDEVICEIDENTIFIER2","directdraw.dddeviceidentifier2"]
old-location: directdraw\dddeviceidentifier2.htm
tech.root: directdraw
ms.assetid: 3fdec953-72d4-48f8-b540-e2e6ca770b3c
ms.date: 12/05/2018
ms.keywords: '*LPDDDEVICEIDENTIFIER2, DDDEVICEIDENTIFIER2, DDDEVICEIDENTIFIER2 structure [DirectDraw], LPDDDEVICEIDENTIFIER2, LPDDDEVICEIDENTIFIER2 structure pointer [DirectDraw], ddraw/DDDEVICEIDENTIFIER2, ddraw/LPDDDEVICEIDENTIFIER2, directdraw.dddeviceidentifier2'
req.header: ddraw.h
req.include-header: 
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
req.typenames: DDDEVICEIDENTIFIER2, *LPDDDEVICEIDENTIFIER2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDDDEVICEIDENTIFIER2
 - ddraw/tagDDDEVICEIDENTIFIER2
 - LPDDDEVICEIDENTIFIER2
 - ddraw/LPDDDEVICEIDENTIFIER2
 - DDDEVICEIDENTIFIER2
 - ddraw/DDDEVICEIDENTIFIER2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddraw.h
api_name:
 - DDDEVICEIDENTIFIER2
---

# DDDEVICEIDENTIFIER2 structure


## -description

The <b>DDDEVICEIDENTIFIER2</b> structure is passed to the <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-getdeviceidentifier">IDirectDraw7::GetDeviceIdentifier</a> method to obtain information about a device.

## -struct-fields

### -field szDriver

Name of the driver.

### -field szDescription

Description of the driver.

### -field liDriverVersion

Version of the driver. It is valid to do less than and greater than comparisons on all 64 bits. Caution should be exercised if you use this element to identify problematic drivers; instead, use the <b>guidDeviceIdentifier</b> member for this purpose.

The data takes the following form:


```

wProduct = HIWORD(liDriverVersion.HighPart)
wVersion = LOWORD(liDriverVersion.HighPart)
wSubVersion = HIWORD(liDriverVersion.LowPart)
wBuild = LOWORD(liDriverVersion.LowPart)

```

### -field dwDriverVersionLowPart

### -field dwDriverVersionHighPart

### -field dwVendorId

Identifier of the manufacturer. Can be 0 if unknown.

### -field dwDeviceId

Identifier of the type of chipset. Can be 0 if unknown.

### -field dwSubSysId

Identifier of the subsystem. Typically, this means the particular board. Can be 0 if unknown.

### -field dwRevision

Identifier of the revision level of the chipset. Can be 0 if unknown.

### -field guidDeviceIdentifier

Unique identifier for the driver and chipset pair. Use this value if you want to track changes to the driver or chipset to reprofile the graphics subsystem. It can also be used to identify particular problematic drivers.

### -field dwWHQLLevel

The Windows Hardware Quality Lab (WHQL) certification level for the device and driver pair.

## -remarks

The values in <b>szDriver</b> and <b>szDescription</b> are for presentation to the user only. They should not be used to identify particular drivers because different strings might be associated with the same device, or the same driver from different vendors might be described differently.



The <b>dwVendorId</b>, <b>dwDeviceId</b>, <b>dwSubSysId</b>, and <b>dwRevision</b> members can be used to identify particular chipsets, but use extreme caution.