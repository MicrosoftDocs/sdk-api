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

# IStreamPseudoRandomBased::get_ExtendedSeed


## -description


Retrieves an array of seed values used by the random number generator.


## -parameters




### -param values [out]

Array of seed values used by the random number generator.


### -param eCount [out]

Number of seed values in the <i>values</i> array.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

Value: 0x80004001

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7630b8ac-41f9-4cc7-95e7-4172a876673f">IStreamPseudoRandomBased</a>



<a href="https://msdn.microsoft.com/c5362760-84c6-4e93-b3cd-2ce568b13102">IStreamPseudoRandomBased::get_Seed</a>



<a href="https://msdn.microsoft.com/a6edf21f-b89a-4780-8065-4d09758fe701">IStreamPseudoRandomBased::put_ExtendedSeed</a>
 

 

