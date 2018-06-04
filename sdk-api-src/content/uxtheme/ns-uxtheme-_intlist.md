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

# _INTLIST structure


## -description


Contains an array or list of <b>int</b> data items from a visual style.


## -struct-fields




### -field iValueCount

Type: <b>int</b>

Number of values in the list.


### -field iValues

Type: <b>int[MAX_INTLIST_COUNT]</b>

List of integers. The constant MAX_INTLIST_COUNT, by definition, is equal to 402 under Windows Vista, but only 10 under earlier versions of Windows.


## -remarks



The lists are returned by <a href="https://msdn.microsoft.com/123ddb53-4447-4b6b-a311-61da47090e94">GetThemeIntList</a>.



