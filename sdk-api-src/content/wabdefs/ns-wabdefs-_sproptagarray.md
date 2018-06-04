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

# _SPropTagArray structure


## -description


Do not use. Contains an array of property tags.


## -struct-fields




### -field cValues

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the number of property tags in the array indicated by the <b>aulPropTag</b> member.


### -field aulPropTag

Type: <b>ULONG[MAPI_DIM]</b>

Array of variables of type <b>ULONG</b> that specify the property tags.

