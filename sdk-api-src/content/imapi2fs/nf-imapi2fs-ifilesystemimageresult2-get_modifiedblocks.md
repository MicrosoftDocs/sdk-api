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

# IFileSystemImageResult2::get_ModifiedBlocks


## -description


Retrieves the list of modified blocks in the result image.


## -parameters




### -param pVal [out]

Pointer to an <a href="https://msdn.microsoft.com/f2a3bd54-4f40-4bf0-9cbf-b507819d669f">IBlockRangeList</a> interface representing the modified block ranges in the result image. 


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



This method returns <b>E_NOTIMPL</b> if the entire result image must be recorded. If this method returns a successful return code, it is sufficient to record only the sectors described by <a href="https://msdn.microsoft.com/f2a3bd54-4f40-4bf0-9cbf-b507819d669f">IBlockRangeList</a> returned in <i>pVal</i>. It is highly recommended to record the sector ranges in exactly the same order as they are listed in <b>IBlockRangeList</b>.




## -see-also




<a href="https://msdn.microsoft.com/83834da1-fa5a-42ef-8e59-7ba133d3e6cb">IFileSystemImageResult2</a>
 

 

