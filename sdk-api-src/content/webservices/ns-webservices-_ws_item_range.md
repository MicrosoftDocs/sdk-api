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

# _WS_ITEM_RANGE structure


## -description



                Defines the minimum and maximum number of items that may appear
                when using <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>, 
                <b>WS_REPEATING_ELEMENT_CHOICE_FIELD_MAPPING</b>,
                or <b>WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING</b> within
                a <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.  The constraint is only
                enforced during deserialization.
            


## -struct-fields




### -field minItemCount

The minimum number of elements that must appear.
                


### -field maxItemCount


                    The maximum number of items that may appear.
                

