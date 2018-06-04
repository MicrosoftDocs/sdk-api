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

# IFaxInboundRouting::GetExtensions


## -description


The <a href="https://msdn.microsoft.com/ecd9a5bb-1624-4cfe-a2d9-b9a5ed722fc4">GetExtensions</a> method retrieves the collection of inbound routing extensions registered with the fax service.


## -parameters




### -param pFaxInboundRoutingExtensions






#### - ppFaxInboundRoutingExtensions [out, retval]

Type: <b><a href="https://msdn.microsoft.com/6daf0614-c0d4-42ba-96de-60f35a39aff1">IFaxInboundRoutingExtensions</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/6daf0614-c0d4-42ba-96de-60f35a39aff1">IFaxInboundRoutingExtensions</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/255706ba-cbbd-4dfa-a9da-95bdd90328b5">IFaxInboundRouting</a>



<a href="https://msdn.microsoft.com/cef24608-cab1-4090-aa94-3a1b76733e98">Visual Basic Example</a>
 

 

