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

# linemessage_tag structure


## -description


The 
<b>LINEMESSAGE</b> structure contains parameter values specifying a change in status of the line the application currently has open. The 
<a href="https://msdn.microsoft.com/ed6df53e-b01d-40bc-8676-b0f7e0eacfd1">lineGetMessage</a> function returns the 
<b>LINEMESSAGE</b> structure.


## -struct-fields




### -field hDevice

Handle to either a line device or a call. The nature of this handle (line handle or call handle) can be determined by the context provided by <i>dwMessageID</i>.


### -field dwMessageID

Line or call device message.


### -field dwCallbackInstance

Instance data passed back to the application, which was specified by the application in the <i>dwCallBackInstance</i> parameter of 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>. This <b>DWORD</b> is not interpreted by TAPI.


### -field dwParam1

Parameter for the message.


### -field dwParam2

Parameter for the message.


### -field dwParam3

Parameter for the message.


## -remarks



For information about parameter values passed in this structure, see 
<a href="https://msdn.microsoft.com/dc11134e-6c20-426e-834e-508bf855e5da">Line Device Messages</a>.




## -see-also




<a href="https://msdn.microsoft.com/ed6df53e-b01d-40bc-8676-b0f7e0eacfd1">lineGetMessage</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>
 

 

