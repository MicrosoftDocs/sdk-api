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

# WS_POLICY_STATE enumeration


## -description



                The state of the policy object.
            


## -enum-fields




### -field WS_POLICY_STATE_CREATED


                    The initial state of the policy object.
                


### -field WS_POLICY_STATE_FAULTED


                    The policy object is no longer usable due to a previous error.
                


## -remarks




                The following diagram illustrates the functions that
                cause state transitions in the policy object.
            

<img alt="" src="images/PolicyStates.png"/>



