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

# _WS_UNIQUE_ID structure


## -description



                Represents a unique ID URI.
            


## -struct-fields




### -field uri


                    A string representation of the URI.  If length is zero,
                    then the unique ID is a guid, and the value is stored
                    in the guid field.  Otherwise, the URI is a string
                    and the string value is stored in the uri field.
                


### -field guid


                    If the uri.length field is 0, then this field contains
                    the GUID representation of the unique ID.  Otherwise
                    the value of the field is not defined.
                


## -remarks




                This structure represents a URI that is used as a unique ID.
                It has native support for GUID-based URI's, but can also
                accommodate other unique-id URI's as a string.
            



