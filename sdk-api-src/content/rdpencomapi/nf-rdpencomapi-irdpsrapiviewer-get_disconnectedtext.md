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

# IRDPSRAPIViewer::get_DisconnectedText


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/6bafe380-2ef4-4e93-a6cd-143798437615">IRDPSRAPIViewer</a> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Retrieves or sets the text that appears centered in the control before a connection is terminated.

This property is read/write.


## -parameters


## -remarks



Setting <b>DisconnectedText</b> is optional. If it is not specified, the control appears blank before a connection is established.

The <b>DisconnectedText</b> property can be set only if the control is not in the connected state. The method returns <b>E_FAIL</b> if it is called after the control is connected.




## -see-also




<a href="https://msdn.microsoft.com/6bafe380-2ef4-4e93-a6cd-143798437615">IRDPSRAPIViewer</a>
 

 

