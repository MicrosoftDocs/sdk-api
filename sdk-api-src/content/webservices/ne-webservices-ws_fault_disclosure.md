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

# WS_FAULT_DISCLOSURE enumeration


## -description



                Controls how much error information is included in a fault.
                Since the error object may contain sensitive
                data as part of the error string, it is not
                always appropriate to include the error strings
                information in all faults.
            


## -enum-fields




### -field WS_MINIMAL_FAULT_DISCLOSURE


                    Use a generic fault string for all errors.
                


### -field WS_FULL_FAULT_DISCLOSURE


                    Use the error string as the fault string.
                

