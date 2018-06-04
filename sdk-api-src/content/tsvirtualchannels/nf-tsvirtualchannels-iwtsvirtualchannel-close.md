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

# IWTSVirtualChannel::Close


## -description


Closes the channel.

If the channel has not already been closed, the <b>Close()</b> method will call the <a href="https://msdn.microsoft.com/5038f2f9-980b-4383-a718-eb4e07e9cfe9">IWTSVirtualChannelCallback::OnClose()</a> method into the associated virtual channel callback interface. After a channel is closed, any <a href="https://msdn.microsoft.com/fef7067c-6d81-42b7-8534-191bc98906d4">Write()</a> call on it will fail.


## -parameters






## -returns



Returns <b>S_OK</b> if successful.




## -see-also




<a href="https://msdn.microsoft.com/8a5b093f-5756-400f-9442-b95d6010ee46">IWTSVirtualChannel</a>
 

 

