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

# _WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE structure


## -description


The <b>WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE</b> structure is used by Windows Media Player to request accelerated metadata synchronization information from portable devices that do not support MTP.


## -struct-fields




### -field dwChangesSinceTransactionID

The transaction identifier supplied by the device during the previous session. This value is zero for the first session ever.


### -field dwResultSetStartingIndex

The index of the first value to retrieve. This value is always zero for the first call of a session.


## -see-also




<a href="https://msdn.microsoft.com/c1d84225-b5b1-4f9e-8694-a229653e53de">Windows Media Device Manager Device Extensions for Metadata Transfer</a>
 

 

