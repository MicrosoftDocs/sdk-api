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

# EngQueryDeviceAttribute function


## -description


The <b>EngQueryDeviceAttribute</b> function allows the driver to query the system about particular attributes of the device.


## -parameters




### -param hdev [in]

Handle to the device. This parameter is the GDI handle received by the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556181">DrvCompletePDEV</a> function.


### -param devAttr [in]

Specifies the attribute for which GDI should return information. This parameter must be QDA_ACCELERATION_LEVEL, which queries the driver accelerations that GDI currently allows.


### -param pvIn [in]

Reserved for system use. This parameter is currently ignored by GDI.


### -param ulInSize [in]

Reserved for system use. This parameter is currently ignored by GDI.


### -param pvOut [out]

Pointer to a buffer of <i>ulOutSize</i> bytes in which GDI writes information about the attribute being queried. When <i>devAttr</i> is QDA_ACCELERATION_LEVEL, GDI writes in the buffer a DWORD value from 0 through 5 that indicates the current acceleration level. See <a href="https://msdn.microsoft.com/b351540d-3459-4ef7-8ab9-8aaebc0c15a9">Display Driver Testing Tools</a> for a description of the acceleration levels.


### -param ulOutSize [out]

Specifies the size, in bytes, of the buffer to which <i>pvOut</i> points.


## -returns



<b>EngQueryDeviceAttribute</b> returns <b>TRUE</b> upon success; otherwise, it returns <b>FALSE</b>.




## -remarks



The video card's acceleration level can be dynamically set through the Display program in Control Panel. <b>EngQueryDeviceAttribute</b> allows the driver to determine the acceleration level currently set.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556252">DrvNotify</a>
 

 

