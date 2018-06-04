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

# _WS_STRING structure


## -description



                An array of Unicode characters and a length.
            


## -struct-fields




### -field length


                    The number of characters in the string.
                


### -field chars


                    The array of characters that make up the string.
                


## -remarks




                The string is not required to be zero terminated.  If it is
                zero terminated, then the terminating character is not included
                in the length.
            


                The macro <a href="https://msdn.microsoft.com/692aa04e-f061-465c-b2ae-27d424d708bc">WS_STRING_VALUE</a> can be used to initialize
                this structure if the string is a constant string.
            



