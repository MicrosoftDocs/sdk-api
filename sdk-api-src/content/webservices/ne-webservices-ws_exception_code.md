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

# WS_EXCEPTION_CODE enumeration


## -description


The structured exception codes thrown by this component.  These
                exceptions are fatal and should not be handled by the application.
            


## -enum-fields




### -field WS_EXCEPTION_CODE_USAGE_FAILURE


                    This exception occurs to indicate that usage of the web services component 
                    has violated the API contract.
                


### -field WS_EXCEPTION_CODE_INTERNAL_FAILURE


                    This exception occurs to indicate that an internal error occurred in the 
                    web services component.
                

