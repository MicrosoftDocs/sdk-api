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

# _WS_XML_CANONICALIZATION_PROPERTY structure


## -description



        Specifies a setting that controls how XML canonicalization is done.
      


## -struct-fields




### -field id


          Identifies the <a href="https://msdn.microsoft.com/af96e1e7-d7e8-4e38-a8ae-f8f28cf0eda9">WS_XML_CANONICALIZATION_PROPERTY_ID</a>.
        


### -field value


            A pointer to the value to set.
            The pointer must have an alignment compatible with the type
            of the property.
        


### -field valueSize


          The size in bytes of the memory pointed to by value.
        

