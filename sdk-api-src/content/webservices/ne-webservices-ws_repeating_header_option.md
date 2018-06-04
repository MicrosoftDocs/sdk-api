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

# WS_REPEATING_HEADER_OPTION enumeration


## -description



                This enum is used to specify whether a header is expected
                to appear more than once in a message.
            


## -enum-fields




### -field WS_REPEATING_HEADER


                    The header may appear more than once in the message.
                


### -field WS_SINGLETON_HEADER


                    The header may appear at most once in the message.
                    When this option is specified, the function 
                    ensures that the specified header appears
                    at most once in the message.
                

