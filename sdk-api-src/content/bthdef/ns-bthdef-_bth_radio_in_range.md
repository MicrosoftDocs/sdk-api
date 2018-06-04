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

# _BTH_RADIO_IN_RANGE structure


## -description


The <b>BTH_RADIO_IN_RANGE</b> structure stores data about Bluetooth devices within communication range.


## -struct-fields




### -field deviceInfo

Current set of attributes associated with the remote device, in the form of a <a href="https://msdn.microsoft.com/b0f2c1fe-1fa0-4816-8471-73fbbced529b">BTH_DEVICE_INFO</a> structure.


### -field previousDeviceFlags

Previous flags for the <b>flags</b> member of the <a href="https://msdn.microsoft.com/b0f2c1fe-1fa0-4816-8471-73fbbced529b">BTH_DEVICE_INFO</a> structure pointed to by the <b>deviceInfo</b> member. Used to determine which attributes associated with the remote device have changed.


## -see-also




<a href="https://msdn.microsoft.com/b0f2c1fe-1fa0-4816-8471-73fbbced529b">BTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/7dab37a6-63ac-4377-9884-61dd19972433">Bluetooth and WM_DEVICECHANGE
				Messages</a>
 

 

