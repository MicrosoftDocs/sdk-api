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

# IItemEnumerator::MoveNext


## -description


Moves the current position to the next item in the enumerator if available.


## -parameters




### -param ItemValid [out]

Returns <b>True</b> if a valid item is found in the position after the move.


## -returns



This method returns an HRESULT value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Indicates success.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  This method always returns <b>S_OK</b> on success, regardless of the state of the enumeration. If there are no more items, <i>ItemValid</i> is set to <b>False</b>, and this is how to determine if the end of the enumeration has been reached.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f43245f1-81d9-4b06-8f0c-d490618a99fa">IItemEnumerator</a>
 

 

