---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION structure


## -description


The DISPLAYCONFIG_SUPPORT_VIRTUAL_RESOLUTION structure contains information on the state of virtual resolution support for the monitor.


## -struct-fields




### -field header

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553920">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that holds information on the type, size, adapterID, and ID of the target the monitor is connected to.


### -field DUMMYSTRUCTNAME

 


### -field DUMMYSTRUCTNAME.DUMMYSTRUCTNAME

 


### -field DUMMYSTRUCTNAME.DUMMYSTRUCTNAME.disableMonitorVirtualResolution

Setting this bit disables virtual mode for the monitor using information found in <b>header</b>.


### -field DUMMYSTRUCTNAME.DUMMYSTRUCTNAME.reserved

Reserved for system use. Do not use in your driver.  


### -field DUMMYSTRUCTNAME.value

Reflects the value of <b>disableMonitorVirtualResolution</b> in cases where debugging is utilized.

