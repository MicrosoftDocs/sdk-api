---
UID: NS:wingdi.DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION
title: DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION
author: windows-sdk-content
description: The DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION structure contains information on the state of virtual resolution support for the monitor.
old-location: display\displayconfig_support_virtual_resolution.htm
tech.root: display
ms.assetid: D9208D00-F437-4B2E-8C39-044F75088659
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION, DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION structure [Display Devices], display.displayconfig_support_virtual_resolution, wingdi/DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 10 Client.
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION
product: Windows
targetos: Windows
req.typenames: DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION
req.redist: 
---

# DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION structure


## -description


The DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION structure contains information on the state of virtual resolution support for the monitor.


## -struct-fields




### -field header

A <a href="https://msdn.microsoft.com/2fdfa54e-2a5f-448f-98e3-e51ce0acaeaf">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that holds information on the type, size, adapterID, and ID of the target the monitor is connected to.


### -field DUMMYSTRUCTNAME

 


### -field DUMMYSTRUCTNAME.DUMMYSTRUCTNAME

 


### -field DUMMYSTRUCTNAME.DUMMYSTRUCTNAME.disableMonitorVirtualResolution

Setting this bit disables virtual mode for the monitor using information found in <b>header</b>.


### -field DUMMYSTRUCTNAME.DUMMYSTRUCTNAME.reserved

Reserved for system use. Do not use in your driver.  


### -field DUMMYSTRUCTNAME.value

Reflects the value of <b>disableMonitorVirtualResolution</b> in cases where debugging is utilized.

