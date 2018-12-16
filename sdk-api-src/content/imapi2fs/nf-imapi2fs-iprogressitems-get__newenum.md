---
UID: NF:imapi2fs.IProgressItems.get__NewEnum
title: IProgressItems::get__NewEnum
author: windows-sdk-content
description: Retrieves the list of progress items from the collection.
old-location: imapi\iprogressitems_get__newenum.htm
tech.root: imapi
ms.assetid: 24528fad-b88c-429a-b5c9-e232e62d3aeb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IProgressItems interface [IMAPI],get__NewEnum method, IProgressItems.get__NewEnum, IProgressItems::get__NewEnum, get__NewEnum, get__NewEnum method [IMAPI], get__NewEnum method [IMAPI],IProgressItems interface, imapi.iprogressitems_get__newenum, imapi2fs/IProgressItems::get__NewEnum
ms.topic: method
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - imapi2fs.h
api_name:
 - IProgressItems.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProgressItems::get__NewEnum


## -description


Retrieves the list of progress items from the collection.


## -parameters




### -param NewEnum [out]

An <b>IEnumVariant</b> interface that you use to enumerate the progress items contained within the collection. Each  item of the enumeration is a VARIANT whose type is <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member to retrieve the <a href="https://msdn.microsoft.com/b6ba9226-655e-4eac-ad43-2b5a8e90039f">IProgressItem</a> interface.


## -returns



S_OK is returned when the number of requested elements (<i>celt</i>) are returned successfully or the number of returned items (<i>pceltFetched</i>) is less than the number of requested elements. The <i>celt</i> and <i>pceltFetched</i> parameters are defined by <b>IEnumVariant</b>.

Other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

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



The enumeration is a snapshot of the progress items contained in the collection at the time of the call.

To retrieve a single item, see the <a href="https://msdn.microsoft.com/74d8e74d-0af6-457a-a16b-f959757b5a86">IProgressItems::get_Item</a> property.




## -see-also




<a href="https://msdn.microsoft.com/30ec514c-97b8-41fc-b814-11f50cacaa25">IFileSystemImageResult</a>



<a href="https://msdn.microsoft.com/b6ba9226-655e-4eac-ad43-2b5a8e90039f">IProgressItem</a>



<a href="https://msdn.microsoft.com/40c28e67-8ff3-4330-90a1-7ebccb0023ad">IProgressItems</a>
 

 

