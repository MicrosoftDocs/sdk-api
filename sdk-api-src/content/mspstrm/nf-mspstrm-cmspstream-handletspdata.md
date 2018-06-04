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

# CMSPStream::HandleTSPData


## -description


The 
<b>HandleTSPData</b> method may be called by the derived call object to let the stream handle the TSP commands. The default implementation returns S_OK. Override this method to implement the stream-specific portion of your MSP-TSP communication. Note that the base call object classes do not call this method; if you want to use it, you must also override the 
<a href="https://msdn.microsoft.com/8f5c31cd-7d74-47d4-9e96-8a965843210c">ReceiveTSPCallData</a> method to dispatch the TSP data to your streams. The stream dispatch information, if any, will be contained in the opaque buffer.


## -parameters




### -param pData

Pointer to opaque buffer containing implementation-dependent information.


### -param dwSize

Size in bytes of opaque buffer.


## -see-also




<a href="https://msdn.microsoft.com/776ca663-faa2-4534-8873-4e20ed79530c">CMSPStream</a>
 

 

