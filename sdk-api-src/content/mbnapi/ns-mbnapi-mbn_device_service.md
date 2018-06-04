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

# MBN_DEVICE_SERVICE structure


## -description


The <b>MBN_DEVICE_SERVICE</b> structure provides information about a Mobile Broadband device service


## -struct-fields




### -field deviceServiceID

A string that represents the unique ID of a Mobile Broadband device service. This matches the Device Service UUID reported by the Mobile Broadband device.


### -field dataWriteSupported

if <b>TRUE</b>, this device service supports write on bulk data sessions. Otherwise, <b>FALSE</b>.


### -field dataReadSupported

if <b>TRUE</b>, this device service supports read on bulk data sessions. Otherwise, <b>FALSE</b>.


## -see-also




<a href="https://msdn.microsoft.com/90CB9B2E-16CA-48A0-AF16-937D816718D6">EnumerateDeviceServices</a>
 

 

