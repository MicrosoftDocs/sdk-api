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

# IWTSVirtualChannelCallback::OnDataReceived


## -description


Notifies the user about data that is being received.

The data has the same size and content as a corresponding <a href="https://msdn.microsoft.com/cb999de8-74a1-4491-bffb-dc4d74a1fea3">WTSVirtualChannelWrite()</a> call from the remote side. There is no hard limit on the size of the data that can be sent. All packet reconstruction is handled by the dynamic virtual channel (DVC) framework.


## -parameters




### -param cbSize [in]

The size, in bytes, of the buffer to receive the data.


### -param pBuffer [in]

A pointer to a buffer to receive the data. This buffer is valid only until this call is complete.


## -returns



Returns <b>S_OK</b> on success. Results in no action if the call fails.




## -see-also




<a href="https://msdn.microsoft.com/d90c6f80-ed4c-4b99-af85-d2c5816ade85">IWTSVirtualChannelCallback</a>
 

 

