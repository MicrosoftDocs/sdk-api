---
UID: NF:winddi.DrvDisableDriver
title: DrvDisableDriver function (winddi.h)
description: The DrvDisableDriver function is used by GDI to notify a driver that it no longer requires the driver and is ready to unload it.
helpviewer_keywords: ["DrvDisableDriver","DrvDisableDriver function [Display Devices]","ddifncs_213ec824-0230-4b4b-879e-ed48401f3788.xml","display.drvdisabledriver","winddi/DrvDisableDriver"]
old-location: display\drvdisabledriver.htm
tech.root: display
ms.assetid: 8f12cc40-6cff-4e40-a264-58d16d3e55bd
ms.date: 12/05/2018
ms.keywords: DrvDisableDriver, DrvDisableDriver function [Display Devices], ddifncs_213ec824-0230-4b4b-879e-ed48401f3788.xml, display.drvdisabledriver, winddi/DrvDisableDriver
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvDisableDriver
 - winddi/DrvDisableDriver
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvDisableDriver
---

# DrvDisableDriver function


## -description

The <b>DrvDisableDriver</b> function is used by GDI to notify a driver that it no longer requires the driver and is ready to unload it.



## -remarks

The driver should free all allocated resources and return the device to the state it was in before the driver was loaded.

<b>DrvDisableDriver</b> is required for graphics drivers.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenabledriver">DrvEnableDriver</a>
