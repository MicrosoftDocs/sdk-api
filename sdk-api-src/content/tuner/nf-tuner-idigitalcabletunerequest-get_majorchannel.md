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

# IDigitalCableTuneRequest::get_MajorChannel


## -description



The <b>get_MajorChannel</b> method retrieves the major channel number.




## -parameters




### -param pMajorChannel [out]

Receives the major channel number. If the value received is BDA_UNDEFINED_CHANNEL, the major channel number is not used.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/75c3c80f-2f02-4cb7-a9e0-aad4076793e4">IDigitalCableTuneRequest Interface</a>
 

 

