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

# IndexedResourceQualifier structure


## -description


Represents the context under which a resource is appropriate.


## -struct-fields




### -field name

The name of the qualifier, such as "language", "contrast", or "scale".


### -field value

The value of the qualifier. You should preserve the case of the qualifier value from the first instance of the qualifier discovered during indexing.



The following values are examples of the qualifier values:

<ul>
<li>"100", "140", or "180" for scale.</li>
<li>"fr-FR" for language.</li>
<li>"high" for contrast.
</li>
</ul>

## -see-also




<a href="https://msdn.microsoft.com/0E1D8CC6-B662-4068-A6BA-822E79321C33">DestroyIndexedResults</a>



<a href="https://msdn.microsoft.com/A1CDA9D1-9FEE-4FCB-AA85-1DA58D9EF95B">IndexFilePath</a>
 

 

