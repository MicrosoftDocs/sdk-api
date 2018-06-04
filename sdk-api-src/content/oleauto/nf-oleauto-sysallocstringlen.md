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

# SysAllocStringLen function


## -description


Allocates a new string, copies the specified number of characters from the passed string, and appends a null-terminating character.


## -parameters




### -param strIn [in]

The input string.


### -param ui [in]

The number of characters to copy. A null character is placed afterwards, allocating a total of <i>ui</i> plus one characters.


## -returns



A copy of the string, or <b>NULL</b> if there is insufficient memory to complete the operation.




## -remarks



The string can contain embedded null characters and does not need to end with a <b>NULL</b>. Free the returned string later with <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>. If <i>strIn</i> is not <b>NULL</b>, then the memory allocated to <i>strIn</i> must be at least <i>ui</i> characters long.

<div class="alert"><b>Note</b>  This function does not convert a <b>char *</b> string into a Unicode <b>BSTR</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/323cefbf-836c-4c9d-bcbe-f2663a57d2b5">String Manipulation Functions</a>
 

 

