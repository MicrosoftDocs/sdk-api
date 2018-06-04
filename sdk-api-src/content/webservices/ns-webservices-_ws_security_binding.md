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

# _WS_SECURITY_BINDING structure


## -description



The abstract base type for all security bindings.  One or more
concrete subtypes of this are specified in the 
<a href="https://msdn.microsoft.com/b9490f00-877c-4d9f-b361-eaca343cdee0">security description</a> that is
supplied during channel and listener creation.  Each concrete subtype
of this corresponds to a security protocol and a way of using it to
provide authentication and/or protection to a channel.
            


Each security binding subtype instance in the security description
contributes one security token at runtime.  Thus, the fields of this
type can be viewed as specifying a security token, how to obtain it,
how to use it for channel security, and how to modify its behavior
using the optional settings.
            


## -struct-fields




### -field bindingType


The<a href="https://msdn.microsoft.com/caa3d71c-420c-4be0-a371-0f2d48ebd757"> WS_SECURITY_BINDING_TYPE</a> of the security binding being described.  The type value
indicates how to obtain the security token corresponding to this
security binding.
                


### -field properties


The array of properties specifying the optional security binding
settings.  Each <a href="https://msdn.microsoft.com/f2790fd7-6f51-45a5-b2b6-e5aaaaca9660">WS_SECURITY_BINDING_PROPERTY</a> in the array is a key-value
pair and must use a key defined in <a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_ID</a>.  This field can be <b>NULL</b>, and if
it is <b>NULL</b>, the default value will be used for each security token
setting.
                


### -field propertyCount


The count of elements in the properties array.
                

