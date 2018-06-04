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

# _TC_IFC_DESCRIPTOR structure


## -description


The 
<b>TC_IFC_DESCRIPTOR</b> structure is an interface identifier used to enumerate interfaces.


## -struct-fields




### -field Length

Number of bytes from the beginning of the 
<b>TC_IFC_DESCRIPTOR</b> to the next 
<b>TC_IFC_DESCRIPTOR</b>.


### -field pInterfaceName

Pointer to a zero-terminated Unicode string representing the name of the packet shaper interface. This name is used in subsequent TC API calls to reference the interface.


### -field pInterfaceID

Pointer to a zero-terminated Unicode string naming the DeviceName of the interface.


### -field AddressListDesc

Network address list descriptor.


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>
 

 

