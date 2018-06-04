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

# ChrCmpIW function


## -description


Performs a comparison between two characters. The comparison is not case-sensitive.


## -parameters




### -param w1 [in]

Type: <b>TCHAR</b>

The first character to be compared.


### -param w2 [in]

Type: <b>TCHAR</b>

The second character to be compared.


## -returns



Type: <b>BOOL</b>

Returns zero if the two characters are the same, or nonzero otherwise.



