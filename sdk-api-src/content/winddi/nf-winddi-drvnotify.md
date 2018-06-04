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

# DrvNotify function


## -description


The <b>DrvNotify</b> function allows a display driver to be notified about certain information by GDI.


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that describes the primary surface for which notification is occurring.


### -param iType

Identifies the type of information about which GDI is notifying the driver. This parameter can be one of the following values:





#### DN_DEVICE_ORIGIN

Notifies the driver of the device's origin. The <i>pvData</i> parameter points to a POINTL structure that identifies the origin of the physical device in desktop space. This notification is useful for drivers of devices that are a part of a multimonitor system. The value to which <i>pvData</i> points is always (0,0) on a single monitor system.



#### DN_DRAWING_BEGIN

Notifies the driver that the first drawing operation is about to occur for this instance of the PDEV that is associated with the specified surface. The <i>pvData</i> parameter points to <b>NULL</b>.


### -param pvData

Pointer to notification data or <b>NULL</b>, depending on the value of <i>iType</i>.


## -returns



None




## -remarks



A display driver can optionally implement <b>DrvNotify</b>. GDI will call <b>DrvNotify</b> only in display drivers that do implement it.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564986">EngQueryDeviceAttribute</a>
 

 

