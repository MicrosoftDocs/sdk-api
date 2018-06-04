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

# TraceLoggingBinary macro


## -description


Wrapper macro for raw binary data.


## -parameters




### -param pbData [in]

The binary data to process.


### -param cbData [in]

The size of the data in bytes.


#### - description [in, optional]

Description of the binary data. This parameter must be a literal string and will be included in the PDB. 


#### - name [in, optional]

The name of the data. This parameter must be a literal string and cannot contain any escape ('/0') characters. 


#### - tags [in, optional]

An integer value. The low 28 bits of the value will be included in the field's metadata and can be used by the event consumer for any purpose.

