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

# _WS_UNIQUE_ID_DESCRIPTION structure


## -description



                
                An optional type description used with <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_UNIQUE_ID_TYPE</a> to specify constraints on the set of values
                which can be deserialized.
            


## -struct-fields




### -field minCharCount


                    The minimum number of characters.  This only pertains 
                    to the case where the unique ID is represented as a string.
                


### -field maxCharCount


                    The maximum number of characters.  This only pertains
                    to the case where the unique ID is represented as a string.
                

