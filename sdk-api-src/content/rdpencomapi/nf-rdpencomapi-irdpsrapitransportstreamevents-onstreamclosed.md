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

# IRDPSRAPITransportStreamEvents::OnStreamClosed


## -description


Notifies the Remote Desktop Protocol (RDP) stack that the connection was closed.


## -parameters




### -param hrReason [in]

Type: <b>HRESULT</b>

An <b>HRESULT</b> value that specifies if the stream was closed normally or due to an error. Contains <b>S_OK</b> if the stream was closed normally or an error code otherwise.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/d38ee3fb-3867-40c9-8e6a-35c94762fdf4">IRDPSRAPITransportStreamEvents</a>
 

 

