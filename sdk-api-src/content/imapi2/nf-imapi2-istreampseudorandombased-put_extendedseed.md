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

# IStreamPseudoRandomBased::put_ExtendedSeed


## -description


Sets a list of seed values for the random number generator and seeks to the start of stream.<div class="alert"><b>Note</b>  This interface is currently not implemented.</div>
<div> </div>



## -parameters




### -param values [in]

Array of seed values used by the random number generator.


### -param eCount [in]

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
 




## -remarks



Use this method to provide a seed value greater than 32 bits. 




## -see-also




<a href="https://msdn.microsoft.com/7630b8ac-41f9-4cc7-95e7-4172a876673f">IStreamPseudoRandomBased</a>



<a href="https://msdn.microsoft.com/e15e47aa-e5c4-4944-a3c4-14e459a31bb5">IStreamPseudoRandomBased::get_ExtendedSeed</a>



<a href="https://msdn.microsoft.com/455d087d-a6f5-45ab-9c0d-c46e721cba6e">IStreamPseudoRandomBased::put_Seed</a>
 

 

