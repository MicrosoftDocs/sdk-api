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

# uaw_wcslen function


## -description


<p class="CCE_Message">[This function is not supported and may be altered or unavailable in the future. Applications should use the <b>wcslen</b> function.]

Retrieves the number of characters in a null-terminated Unicode string.


## -parameters




### -param String [in]

A pointer to a null-terminated Unicode string.


## -returns



The return value is the number of characters in <i>String</i>, not including the terminating null character.




## -remarks



This function is available only on 64-bit Windows.



