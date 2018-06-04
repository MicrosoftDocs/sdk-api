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

# ITMediaControl::get_MediaState


## -description


The 
<b>get_MediaState</b> method gets the current state of media on the file terminal.


## -parameters




### -param pTerminalMediaState [out]

Pointer to the 
<a href="https://msdn.microsoft.com/9cc07684-9804-41ac-bc25-f37f6ae00280">TERMINAL_MEDIA_STATE</a> descriptor of the current state of the file terminal.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/016166a1-72ac-4ce8-9c86-43cf94b1bdbd">ITMediaControl</a>



<a href="https://msdn.microsoft.com/9cc07684-9804-41ac-bc25-f37f6ae00280">TERMINAL_MEDIA_STATE</a>
 

 

