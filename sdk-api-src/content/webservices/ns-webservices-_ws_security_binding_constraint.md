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

# _WS_SECURITY_BINDING_CONSTRAINT structure


## -description



                The base class for all security binding constraint structures.
            


## -struct-fields




### -field type


                    This value depends on which type of security binding constraint that is used.
                


### -field propertyConstraints


                    A set of binding-specific security property constraints.
                


                    See <a href="https://msdn.microsoft.com/97334ced-315d-49db-9c7b-b05ef387f6c8">WS_SECURITY_BINDING_PROPERTY_CONSTRAINT</a> for more information.
                


### -field propertyConstraintCount


                    The number of elements in the propertyConstraints array.
                


                    If the array has zero elements, the propertyConstraints field may be <b>NULL</b>.
                

