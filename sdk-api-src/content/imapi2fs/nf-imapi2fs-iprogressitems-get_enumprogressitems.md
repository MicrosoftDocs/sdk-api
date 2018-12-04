---
UID: NF:imapi2fs.IProgressItems.get_EnumProgressItems
title: IProgressItems::get_EnumProgressItems
author: windows-sdk-content
description: Retrieves the list of progress items from the collection.
old-location: imapi\iprogressitems_get_enumprogressitems.htm
tech.root: imapi
ms.assetid: 746b05b7-ddba-458c-bc9b-4913da5fa8b5
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IProgressItems interface [IMAPI],get_EnumProgressItems method, IProgressItems.get_EnumProgressItems, IProgressItems::get_EnumProgressItems, get_EnumProgressItems, get_EnumProgressItems method [IMAPI], get_EnumProgressItems method [IMAPI],IProgressItems interface, imapi.iprogressitems_get_enumprogressitems, imapi2fs/IProgressItems::get_EnumProgressItems
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
 - IProgressItems.get_EnumProgressItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProgressItems::get_EnumProgressItems


## -description


Retrieves the list of progress items from the collection.


## -parameters




### -param NewEnum [out]

An <a href="https://msdn.microsoft.com/c4238fbe-762a-492f-9eb5-d927e64436e1">IEnumProgressItems</a> interface that contains a collection of the progress items contained in the collection.


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



This property returns the same results as the <a href="https://msdn.microsoft.com/24528fad-b88c-429a-b5c9-e232e62d3aeb">IProgressItems::get__NewEnum</a> property and is meant for use by C/C++ applications.




## -see-also




<a href="https://msdn.microsoft.com/c4238fbe-762a-492f-9eb5-d927e64436e1">IEnumProgressItems</a>



<a href="https://msdn.microsoft.com/40c28e67-8ff3-4330-90a1-7ebccb0023ad">IProgressItems</a>
 

 

