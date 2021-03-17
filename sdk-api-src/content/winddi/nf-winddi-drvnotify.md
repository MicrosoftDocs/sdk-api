---
UID: NF:winddi.DrvNotify
title: DrvNotify function (winddi.h)
description: The DrvNotify function allows a display driver to be notified about certain information by GDI.
helpviewer_keywords: ["DrvNotify","DrvNotify function [Display Devices]","ddifncs_24141fb1-e368-47f8-b123-eb1e1789b568.xml","display.drvnotify","winddi/DrvNotify"]
old-location: display\drvnotify.htm
tech.root: display
ms.assetid: 792d2b17-d5f5-406e-b35c-9f641fa32016
ms.date: 12/05/2018
ms.keywords: DrvNotify, DrvNotify function [Display Devices], ddifncs_24141fb1-e368-47f8-b123-eb1e1789b568.xml, display.drvnotify, winddi/DrvNotify
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
 - DrvNotify
 - winddi/DrvNotify
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
 - DrvNotify
---

# DrvNotify function


## -description

The <b>DrvNotify</b> function allows a display driver to be notified about certain information by GDI.

## -parameters

### -param pso

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the primary surface for which notification is occurring.

### -param iType

Identifies the type of information about which GDI is notifying the driver. This parameter can be one of the following values:





#### DN_DEVICE_ORIGIN

Notifies the driver of the device's origin. The <i>pvData</i> parameter points to a POINTL structure that identifies the origin of the physical device in desktop space. This notification is useful for drivers of devices that are a part of a multimonitor system. The value to which <i>pvData</i> points is always (0,0) on a single monitor system.



#### DN_DRAWING_BEGIN

Notifies the driver that the first drawing operation is about to occur for this instance of the PDEV that is associated with the specified surface. The <i>pvData</i> parameter points to <b>NULL</b>.

### -param pvData

Pointer to notification data or <b>NULL</b>, depending on the value of <i>iType</i>.

## -remarks

A display driver can optionally implement <b>DrvNotify</b>. GDI will call <b>DrvNotify</b> only in display drivers that do implement it.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engquerydeviceattribute">EngQueryDeviceAttribute</a>