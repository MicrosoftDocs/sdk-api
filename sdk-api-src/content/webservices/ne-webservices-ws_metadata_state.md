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

# WS_METADATA_STATE enumeration


## -description



                The state of the metadata object.
            


## -enum-fields




### -field WS_METADATA_STATE_CREATED

The initial state of the metadata object.
                


### -field WS_METADATA_STATE_RESOLVED


                    All references between metadata documents have been
                    resolved and no more metadata documents may be added
                    to the metadata object.  See <a href="https://msdn.microsoft.com/1cf9f2ba-c303-4668-a959-8fad69746438">WsGetMetadataEndpoints</a> for
                    more information.
                


### -field WS_METADATA_STATE_FAULTED


                    The metadata object not usable due to a previous error.  See
                    See <a href="https://msdn.microsoft.com/1cf9f2ba-c303-4668-a959-8fad69746438">WsGetMetadataEndpoints</a> and <a href="https://msdn.microsoft.com/0b824948-e06d-482d-8d53-c4e27d1ecf0f">WsReadMetadata</a>
                    for more information.
                


## -remarks




                The following diagram illustrates the functions that 
                cause state transitions in the metadata object.
            

<img alt="" src="images/MetadataStates.png"/>



