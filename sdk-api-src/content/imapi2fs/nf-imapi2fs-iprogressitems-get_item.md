---
UID: NF:imapi2fs.IProgressItems.get_Item
title: IProgressItems::get_Item
author: windows-driver-content
description: Retrieves the specified progress item from the collection.
old-location: imapi\iprogressitems_get_item.htm
old-project: imapi
ms.assetid: 74d8e74d-0af6-457a-a16b-f959757b5a86
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IProgressItems interface [IMAPI],get_Item method, IProgressItems.get_Item, IProgressItems::get_Item, get_Item, get_Item method [IMAPI], get_Item method [IMAPI],IProgressItems interface, imapi.iprogressitems_get_item, imapi2fs/IProgressItems::get_Item
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PlatformId
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2fs.h
api_name:
-	IProgressItems.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IProgressItems::get_Item


## -description


Retrieves the specified progress item from the collection.


## -parameters




### -param Index [in]

Zero-based index number corresponding to a progress item in the collection.


### -param item [out]

An <a href="https://msdn.microsoft.com/b6ba9226-655e-4eac-ad43-2b5a8e90039f">IProgressItem</a> interface associated with the specified index value.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

Value: 0x80070057

</td>
</tr>
</table>
 




## -remarks



To enumerate all progress items, call the <a href="https://msdn.microsoft.com/24528fad-b88c-429a-b5c9-e232e62d3aeb">IProgressItems::get__NewEnum</a> method.




## -see-also




<a href="https://msdn.microsoft.com/b6ba9226-655e-4eac-ad43-2b5a8e90039f">IProgressItem</a>



<a href="https://msdn.microsoft.com/40c28e67-8ff3-4330-90a1-7ebccb0023ad">IProgressItems</a>



<a href="https://msdn.microsoft.com/2b37cf63-24be-42ff-a439-157703db9604">IProgressItems::ProgressItemFromBlock</a>



<a href="https://msdn.microsoft.com/c27e9f30-e3f1-4436-b33a-fa3130baf374">IProgressItems::ProgressItemFromDescription</a>
 

 

