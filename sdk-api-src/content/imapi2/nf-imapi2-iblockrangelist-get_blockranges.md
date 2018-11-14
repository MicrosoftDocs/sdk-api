---
UID: NF:imapi2.IBlockRangeList.get_BlockRanges
title: IBlockRangeList::get_BlockRanges
author: windows-sdk-content
description: Returns the list of sector ranges in the form of a safe array of variants of type VT_Dispatch.
old-location: imapi\iblockrangelist_get_blockranges.htm
tech.root: imapi
ms.assetid: b9c7e4ee-0fb2-4a15-8277-8db82a4f3afe
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IBlockRangeList interface [IMAPI],get_BlockRanges method, IBlockRangeList.get_BlockRanges, IBlockRangeList::get_BlockRanges, get_BlockRanges, get_BlockRanges method [IMAPI], get_BlockRanges method [IMAPI],IBlockRangeList interface, imapi.iblockrangelist_get_blockranges, imapi2/IBlockRangeList::get_BlockRanges
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IBlockRangeList.get_BlockRanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2.h
: 
- IBlockRangeList.get_BlockRanges
: 
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
 

 

