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

# IBDA_Topology::SetMedium


## -description



The <b>SetMedium</b> method configures the medium on which a particular pin sends data.




## -parameters




### -param ulPinId [in]

Specifies the identifier of the pin on which to set the medium.


### -param pMedium [in]

Pointer to the medium on which the pin will send data.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



A medium is a structure that identifies a hardware data path between two devices on the host system. They can be devices on the same card, such as a crossbar and a tuner on a TV card; devices on separate cards; or external devices. Kernel-mode filters based on the Windows Driver Model can use mediums instead of media types to determine pin connections.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/35dfe39e-05b4-4c7b-9358-081429b064f2">IBDA_Topology Interface</a>
 

 

