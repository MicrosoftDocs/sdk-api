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

# _WS_SERVICE_CONTRACT structure


## -description



                Specifies a service contract on an <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">endpoint</a>.
            


## -struct-fields




### -field contractDescription


                    The typed contract metadata. See <a href="https://msdn.microsoft.com/0b2a5516-6faf-43d5-9370-a25dbc7e2843">WS_CONTRACT_DESCRIPTION</a>. Optional, if <b>defaultMessageHandlerCallback</b> is given.
                


### -field defaultMessageHandlerCallback


                    Callback for processing unhandled messages. Optional if contractDescription is given. 
                


### -field methodTable


                    The function table. Mandatory, if <b>contractDescription</b> is given.
                

