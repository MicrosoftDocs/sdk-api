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

# PFN_WdsTransportClientReceiveMetadata callback function


## -description


PFN_WdsTransportClientReceiveMetadata is an optional callback that a consumer may register to receive metadata type information about a file.  This information is provided by the content provider and is opaque to the multicast client and server.


## -parameters




### -param hSessionKey [in]

The handle belonging to the session that is being started.


### -param pCallerData [in]

Pointer to the caller specific data for this session.    This data was specified in the call to <a href="https://msdn.microsoft.com/aa89899f-8f50-4617-84a1-4013412f0292">WdsTransportClientStartSession</a> function.


### -param pMetadata [in]

Data provided by the content provider that is associated with this object in some manner. 


### -param ulSize [in]

The size of the <i>pMetadata</i> buffer in bytes.


## -returns



This callback function does not return a value.



