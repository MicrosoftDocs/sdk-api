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

# _WS_HTTP_HEADER_MAPPING structure


## -description



                Specifies an individual header that is mapped as part of <a href="https://msdn.microsoft.com/dff8217e-769d-4f0b-acf2-02d6e43589cf">WS_HTTP_MESSAGE_MAPPING</a>.
            


## -struct-fields




### -field headerName


                    The name of the HTTP header.
                


### -field headerMappingOptions


                    A set of flags that control how headers are mapped.  
                    See <a href="https://msdn.microsoft.com/cd11cae2-36af-4086-80f3-e99493bf9eb1">WS_HTTP_HEADER_MAPPING_OPTIONS</a> for more information.
                

