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

# midiopendesc_tag structure


## -description


The <code>MIDIOPENDESC</code> structure is a client-filled structure that provides information about how to open a MIDI device.


## -struct-fields




### -field hMidi

Specifies the handle that the client uses to reference the device. This handle is assigned by WINMM. Use this handle when you notify the client with the <a href="http://go.microsoft.com/fwlink/p/?linkid=142261">DriverCallback</a> function.


### -field dwCallback

Specifies either the address of a callback function, a window handle, or a task handle, depending on the flags that are specified in the dwParam2 parameter of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff537541">MODM_OPEN</a> message. If this field contains a handle, it is contained in the low-order word.


### -field dwInstance

Specifies a pointer to a DWORD that contains instance information for the client. This instance information is returned to the client whenever the driver notifies the client by using the <b>DriverCallback</b> function.


### -field dnDevNode

Specifies a device node for the MIDI output device, if it is a Plug and Play (PnP) MIDI device.


### -field cIds

Specifies the number of stream identifiers, if a stream is open.


### -field rgIds

Specifies an array of device identifiers. The number of identifiers is given by the <b>cIds</b> member.


## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=142261">DriverCallback</a>
 

 

