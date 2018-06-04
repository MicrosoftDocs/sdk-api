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

# RtlInitUnicodeString function


## -description


Initializes a counted Unicode string.  


## -parameters




### -param DestinationString [in, out]

The buffer for a counted Unicode string to be initialized. The length is initialized to zero if the <i>SourceString</i> is not specified. 


### -param SourceString [in, optional]

Optional pointer to a null-terminated Unicode string with
        which to initialize the counted string. 


## -returns



This function does not return a value.



