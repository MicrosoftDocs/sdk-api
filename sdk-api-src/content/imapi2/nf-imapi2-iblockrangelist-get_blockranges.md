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

# IBlockRangeList::get_BlockRanges


## -description


Returns the list of sector ranges in the form of a safe array of variants of type VT_Dispatch.


## -parameters




### -param value [out, retval]

List of sector ranges. Each element of the list is a VARIANT of type VT_Dispatch. Query the pdispVal member of the variant for the <a href="https://msdn.microsoft.com/abebc651-0575-4b76-9fe8-2cea3d617582">IBlockRange</a> interface. 


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
</table>
 




## -remarks



The order of sector ranges in <a href="https://msdn.microsoft.com/f2a3bd54-4f40-4bf0-9cbf-b507819d669f">IBlockRangeList</a> is taken into account during burning. The sector ranges having lower indexes in the safe array returned by <b>IBlockRangeList::get_BlockRanges</b> are written before those with higher indexes.




## -see-also




<a href="https://msdn.microsoft.com/f2a3bd54-4f40-4bf0-9cbf-b507819d669f">IBlockRangeList</a>
 

 

