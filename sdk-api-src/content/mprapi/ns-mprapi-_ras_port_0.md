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

# _RAS_PORT_0 structure


## -description


The 
<b>RAS_PORT_0</b> structure contains general information regarding a specific RAS port, such as port condition and port name. For more detailed information about a specific port, such as line speed or errors, see 
<a href="https://msdn.microsoft.com/4850f08e-13ee-485f-99a5-be4554d6311b">RAS_PORT_1</a>.


## -struct-fields




### -field hPort

Handle to the port.


### -field hConnection

Handle to the connection.


### -field dwPortCondition


<a href="https://msdn.microsoft.com/86bcca08-97c5-404c-b5d9-a90d93f26e00">RAS_PORT_CONDITION</a> structure.


### -field dwTotalNumberOfCalls

Specifies the cumulative number of calls this port has serviced.


### -field dwConnectDuration

Specifies the duration of the current connection, in seconds.


### -field wszPortName

Specifies the port name.


### -field wszMediaName

Specifies the media name.


### -field wszDeviceName

Specifies the device name.


### -field wszDeviceType

Specifies the device type.


## -see-also




<a href="https://msdn.microsoft.com/858fcdd8-6587-41c4-a2d7-c871722562e7">RAS
		  Administration Structures</a>



<a href="https://msdn.microsoft.com/4850f08e-13ee-485f-99a5-be4554d6311b">RAS_PORT_1</a>



<a href="https://msdn.microsoft.com/86bcca08-97c5-404c-b5d9-a90d93f26e00">RAS_PORT_CONDITION</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

