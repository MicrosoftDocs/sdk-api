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

# _WS_ANY_ATTRIBUTES structure


## -description



                This type is used to store a set of attributes
                that have not been directly mapped to field of 
                a structure.
            


## -struct-fields




### -field attributes


                    An array of attributes.  This field may
                    be <b>NULL</b> if attributeCount is zero.
                


### -field attributeCount


                    The number of attributes in the array.
                


## -remarks




                This structure is typically used to preserve unknown attributes
                when deserializing a structure.
                See <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ANY_ATTRIBUTES_FIELD_MAPPING</a>
                and <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_ANY_ATTRIBUTES_TYPE</a> for more
                information.
            



