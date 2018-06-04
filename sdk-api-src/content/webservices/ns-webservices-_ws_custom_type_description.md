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

# _WS_CUSTOM_TYPE_DESCRIPTION structure


## -description


Represents a custom mapping between a C data type and an XML element.
                User-defined callbacks are invoked to do the actual reading and
                writing.
            


## -struct-fields




### -field size


                    The size of the custom type, in bytes.
                


### -field alignment


                    The alignment requirement of the custom type.  This must be a
                    power of two between 1 and 8.
                


### -field readCallback

A pointer to a callback which is invoked to read the type.


### -field writeCallback

A pointer to a callback which is invoked to write the type.


### -field descriptionData


                    This can be used to point to additional user-defined data
                    specific to the type.  It is optional and may be <b>NULL</b>.
                


                    The pointer to this data is passed
                    to the <a href="https://msdn.microsoft.com/95df152c-69cb-4417-9e85-e7ecb54ed042">WS_READ_TYPE_CALLBACK</a> and the
                    <a href="https://msdn.microsoft.com/f94bdf80-abea-4a97-9d41-add498e314b1">WS_WRITE_TYPE_CALLBACK</a>.  This allows the
                    callback to access information that is specific to this
                    particular usage of the callback.
                


### -field isDefaultValueCallback

 



