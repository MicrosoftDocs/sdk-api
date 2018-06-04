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

# WdsTransportClientCompleteReceive function


## -description


Indicates that all processing on a block of data is finished, and that the multicast client may purge this block of data from its cache to make room for further receives.


## -parameters




### -param hSessionKey [in]

Unique handle returned by the call to <a href="https://msdn.microsoft.com/0ece4ac8-372c-46ec-a6a1-ff1b547a85ef">WdsTransportClientInitializeSession</a>.


### -param ulSize [in]

The size of the block being released.


### -param pullOffset [in]

The offset of the block being released.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -remarks



There must be one call to <b>WdsTransportClientCompleteReceive</b> for each call to the <a href="https://msdn.microsoft.com/3a1cd9bb-c0da-4d66-9338-1f284fc15499">PFN_WdsTransportClientReceiveContents</a> callback that the consumer receives.  The length and offset parameters of this function call must match those provided in the receive contents callback.  Failure to call this function will result in a stall in the multicast client once it hits the cache limit specified by the <i>ulCacheSize</i> of the <a href="https://msdn.microsoft.com/efa1ea12-5234-474b-a859-cd074290e375">WDS_TRANSPORTCLIENT_REQUEST</a> structure passed to <a href="https://msdn.microsoft.com/0ece4ac8-372c-46ec-a6a1-ff1b547a85ef">WdsTransportClientInitializeSession</a>.



