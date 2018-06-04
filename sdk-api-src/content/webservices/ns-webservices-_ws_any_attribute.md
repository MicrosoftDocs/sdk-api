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

# _WS_ANY_ATTRIBUTE structure


## -description



                This type is used to store an attribute
                that has not been directly mapped to a field.
            


## -struct-fields




### -field localName


                    Specifies the localName of the attribute.
                


### -field ns


                    Specifies the namespace of the attribute.
                


### -field value


                    Specifies the value of the attribute.  This
                    field may not be <b>NULL</b>.
                


## -remarks




                This structure is used with <a href="https://msdn.microsoft.com/6c428c99-755f-40ab-bc9e-e1a7a3d70c1d">WS_ANY_ATTRIBUTES</a>.
            



