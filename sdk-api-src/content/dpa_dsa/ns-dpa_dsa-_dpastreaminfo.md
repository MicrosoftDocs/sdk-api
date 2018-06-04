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

# _DPASTREAMINFO structure


## -description


Contains a stream item used by the <a href="https://msdn.microsoft.com/b5910ac3-9066-49d8-8cb3-796de22428d3">PFNDPASTREAM</a> callback function. 


## -struct-fields




### -field iPos

Type: <b>int</b>

An index of the item in the DPA. 


### -field pvItem

Type: <b>void*</b>

A void pointer to the item data. 

