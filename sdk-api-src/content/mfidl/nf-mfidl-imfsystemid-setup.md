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

# IMFSystemId::Setup


## -description


Sets up the <a href="https://msdn.microsoft.com/45c80fc5-5ea7-4d4e-9c9c-5a38f62b2d28">IMFSystemId</a>.


## -parameters




### -param stage

Stage in the setup process. 0 or 1.


### -param cbIn

Size of the input buffer.


### -param pbIn

The input buffer.


### -param pcbOut

Size of output buffer.


### -param ppbOut

The output buffer.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/45c80fc5-5ea7-4d4e-9c9c-5a38f62b2d28">IMFSystemId</a>
 

 

