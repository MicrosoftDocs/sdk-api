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

# _TCI_CLIENT_FUNC_LIST structure


## -description


The 
<b>TCI_CLIENT_FUNC_LIST</b> structure is used by the traffic control interface to register and then access client-callback functions. Each member of 
<b>TCI_CLIENT_FUNC_LIST</b> is a pointer to the client provided–callback function.


## -struct-fields




### -field ClNotifyHandler

Pointer to the client-callback function 
<a href="https://msdn.microsoft.com/cacf4c21-d831-462c-b9e8-fd51fcf8e4e4">ClNotifyHandler</a>
			.


### -field ClAddFlowCompleteHandler

Pointer to the client-callback function <a href="https://msdn.microsoft.com/0aa6f590-f7b2-4312-87a7-3854f883fa22">ClAddFlowComplete</a>.


### -field ClModifyFlowCompleteHandler

Pointer to the client-callback function <a href="https://msdn.microsoft.com/61afc465-d942-4db7-96ee-56f3f1c3cafa">ClModifyFlowComplete</a>
			.


### -field ClDeleteFlowCompleteHandler

Pointer to the client-callback function <a href="https://msdn.microsoft.com/b31bd6e5-2b72-407d-a77e-ff9cee8de238">ClDeleteFlowComplete</a>.


## -remarks



Any member of the 
<b>TCI_CLIENT_FUNC_LIST</b> structure can be <b>NULL</b> except <b>ClNotifyHandler</b>.




## -see-also




<a href="https://msdn.microsoft.com/0aa6f590-f7b2-4312-87a7-3854f883fa22">ClAddFlowComplete</a>



<a href="https://msdn.microsoft.com/b31bd6e5-2b72-407d-a77e-ff9cee8de238">ClDeleteFlowComplete</a>



<a href="https://msdn.microsoft.com/61afc465-d942-4db7-96ee-56f3f1c3cafa">ClModifyFlowComplete</a>



<a href="https://msdn.microsoft.com/cacf4c21-d831-462c-b9e8-fd51fcf8e4e4">ClNotifyHandler</a>
 

 

