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

# tag_WBEM_REFRESHER_FLAGS enumeration


## -description


Contains flags that modify the behavior of refresher methods.


## -enum-fields




### -field WBEM_FLAG_REFRESH_AUTO_RECONNECT

If the connection is broken, the refresher attempts to reconnect to the provider automatically.


### -field WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT

If the connection is broken, the refresher does not attempt to reconnect to the provider automatically.


## -see-also




<a href="https://msdn.microsoft.com/f6e68b95-e9d1-473e-add4-823b6db51709">IWbemConfigureRefresher::Remove</a>



<a href="https://msdn.microsoft.com/6de85040-c938-41dc-8240-0e21e89c7716">IWbemRefresher::Refresh</a>
 

 

