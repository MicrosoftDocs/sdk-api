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

# ITraceDataProvider::Query


## -description


Retrieves details about a registered provider.


## -parameters




### -param bstrName [in]

The name of the registered provider. The name is case-insensitive. You can also specify the string form of the provider's GUID.


### -param bstrServer [in]

The computer on which the provider is registered. You can specify the computer's name, fully qualified domain name, or IP address.


## -returns



Returns S_OK if successful.




## -remarks



To specify kernel providers, set the <i>bstrName</i> parameter to "Windows Kernel Trace".

To specify the context logger, set <i>bstrName</i> to "Circular Kernel Context Logger". The context logger provides a snapshot of the current state of the computer. The logger writes to an in-memory 100-megabyte circular log (not to a file). To release its contents to consumers, call the <a href="https://msdn.microsoft.com/7e432e1f-4b86-45dc-93d5-df603068273d">IDataCollectorSet::Commit</a> method to flush the session.




## -see-also




<a href="https://msdn.microsoft.com/bd2a49c1-8e18-4a14-a797-07f2b9c25812">ITraceDataProvider</a>
 

 

