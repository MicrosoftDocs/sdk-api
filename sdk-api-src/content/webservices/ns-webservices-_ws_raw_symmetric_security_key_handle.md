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

# _WS_RAW_SYMMETRIC_SECURITY_KEY_HANDLE structure


## -description



The type for specifying a symmetric cryptographic key as raw bytes.
            


## -struct-fields




### -field keyHandle


The base type from which this type and all other key handle types derive.
                


### -field rawKeyBytes


The cryptographic key as raw bytes.  It is strongly recommended that
after the key is supplied in this form to any API, it is immediately
cleared using SecureZeroMemory.
                

