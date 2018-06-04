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

# IPBDASiParser::GetServices


## -description


Retrieves a list of services from the  program and system information protocol (PSIP) tables in a Protected Broadcast  Device Architecture (PBDA) transport stream.


## -parameters




### -param dwSize [in]

Size of the buffer that receives the service list, in bytes.


### -param pBuffer [in]

Receives the buffer for services.


### -param ppServices [out]

Receives an <a href="https://msdn.microsoft.com/8d2d62cd-9f62-45d3-8b98-74bb8863c6d6">IPBDA_Services</a> interface pointer.  The caller must release this interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a1cc25ec-b519-4c24-ba85-f2c240749fbd">IPBDASiParser</a>



<a href="https://msdn.microsoft.com/8d2d62cd-9f62-45d3-8b98-74bb8863c6d6">IPBDA_Services</a>
 

 

