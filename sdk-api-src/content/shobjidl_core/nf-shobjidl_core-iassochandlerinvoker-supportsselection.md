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

# IAssocHandlerInvoker::SupportsSelection


## -description


Determines whether an invoker supports its selection.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if this instance supports its selection, or <b>S_FALSE</b> otherwise.




## -remarks



For example, this method should return whether an application (as selected from an "Open With" context menu) can <b>Open</b> a file.
             



