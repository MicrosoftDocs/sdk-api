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

# _WS_PARAMETER_DESCRIPTION structure


## -description



                The index of the parameters in the incoming/outgoing messages field descriptions. 
            


## -struct-fields




### -field parameterType


                    The type of the parameter.
                


### -field inputMessageIndex

A value between 0 and MAX_SHORT - 1 that represents the index of the field 
                    in the input <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a>. It is MAX_USHORT if it has not present in the input
                    WS_MESSAGE. 
                


### -field outputMessageIndex


                    A value between 0 and MAX_SHORT - 1 that represents the index of the field 
                    in the output <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a>. It is MAX_USHORT if it has not present in the output
                    WS_MESSAGE. 
                

