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

# berval structure


## -description


The <b>berval</b> structure represents arbitrary binary data that is encoded according to Basic Encoding Rules (BER). Use a <b>berval</b> to represent any attribute that cannot be represented by a null-terminated string.


## -struct-fields




### -field bv_len

Length, in bytes,  of binary data.


### -field bv_val

Pointer to the binary data.


## -remarks



Use a <b>berval</b> structure for attributes that contain raw binary data, such as certificates, graphics, or sound files.




## -see-also




<a href="https://msdn.microsoft.com/1af7ea80-a65b-42bf-a1b2-ca54c173c9fb">Data Structures</a>
 

 

