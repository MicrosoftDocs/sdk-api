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

# DWRITE_TRIMMING_GRANULARITY enumeration


## -description


Specifies  the text granularity used to trim text overflowing the layout box.


## -enum-fields




### -field DWRITE_TRIMMING_GRANULARITY_NONE

No trimming occurs. Text flows beyond the layout width.


### -field DWRITE_TRIMMING_GRANULARITY_CHARACTER

Trimming occurs at a character cluster boundary.


### -field DWRITE_TRIMMING_GRANULARITY_WORD

Trimming occurs at a word boundary.

