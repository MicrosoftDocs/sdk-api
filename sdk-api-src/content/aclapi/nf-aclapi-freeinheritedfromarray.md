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

# FreeInheritedFromArray function


## -description



			The <b>FreeInheritedFromArray</b> function frees memory allocated by the 
<a href="https://msdn.microsoft.com/ccc1702b-e414-4831-ae8b-fd92499bec94">GetInheritanceSource</a> function.


## -parameters




### -param pInheritArray [in]

A pointer to the array of <a href="https://msdn.microsoft.com/6839f67a-6c72-406d-b55e-bc366aaad107">INHERITED_FROM</a> structures returned by <a href="https://msdn.microsoft.com/ccc1702b-e414-4831-ae8b-fd92499bec94">GetInheritanceSource</a>.


### -param AceCnt [in]

Number of entries in <i>pInheritArray</i>.


### -param OPTIONAL

TBD




#### - pfnArray [in, optional]

Unused. Set to <b>NULL</b>.


## -returns




						If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/ccc1702b-e414-4831-ae8b-fd92499bec94">GetInheritanceSource</a>
 

 

