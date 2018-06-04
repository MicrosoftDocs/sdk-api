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

# SHDestroyPropSheetExtArray function


## -description


<p class="CCE_Message">[<b>SHDestroyPropSheetExtArray</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Frees property sheet handlers that are pointed to an array created by <a href="https://msdn.microsoft.com/88a72529-325d-431e-bc26-bddca787e62b">SHCreatePropSheetExtArray</a>.


## -parameters




### -param hpsxa [in]

Type: <b>HPSXA</b>

The handle of the array that contains pointers to the property sheet handlers to destroy.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/e0570cd6-dda2-43e4-8540-58baef37bf18">SHAddFromPropSheetExtArray</a>



<a href="https://msdn.microsoft.com/88a72529-325d-431e-bc26-bddca787e62b">SHCreatePropSheetExtArray</a>



<a href="https://msdn.microsoft.com/a8bdde44-d668-46c4-9e58-7a45b775fe09">SHReplaceFromPropSheetExtArray</a>
 

 

