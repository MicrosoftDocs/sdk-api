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

# tagHITRANGE structure


## -description


Identifies the range of matching data when query search conditions match indexed data.


## -struct-fields




### -field iPosition

Type: <b>ULONG</b>

The beginning of the hit range.


### -field cLength

Type: <b>ULONG</b>

The length of the hit range.


## -remarks



The <b>HITRANGE</b> structure is useful for identifying where a search term matches the content from returned results, and for hit highlighting in user interfaces.



