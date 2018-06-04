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

# _ADRLIST structure


## -description


Do not use. Describes zero or more properties belonging to one or more recipients. 



## -struct-fields




### -field cEntries

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the entry count in the array specified by the <b>aEntries</b> member.


### -field aEntries

Type: <b><a href="https://msdn.microsoft.com/3044ca5e-f802-4c7b-8521-7d8adc63dc1b">ADRENTRY</a>[MAPI_DIM]</b>

Variable of type <a href="https://msdn.microsoft.com/3044ca5e-f802-4c7b-8521-7d8adc63dc1b">ADRENTRY</a> that specifies the array of <b>ADRENTRY</b> structures, one structure for each recipient.

