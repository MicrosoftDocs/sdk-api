---
UID: NF:imapi2fs.IProgressItems.ProgressItemFromDescription
title: IProgressItems::ProgressItemFromDescription
author: windows-sdk-content
description: Retrieves a progress item based on the specified file name.
old-location: imapi\iprogressitems_progressitemfromdescription.htm
tech.root: imapi
ms.assetid: c27e9f30-e3f1-4436-b33a-fa3130baf374
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IProgressItems interface [IMAPI],ProgressItemFromDescription method, IProgressItems.ProgressItemFromDescription, IProgressItems::ProgressItemFromDescription, ProgressItemFromDescription, ProgressItemFromDescription method [IMAPI], ProgressItemFromDescription method [IMAPI],IProgressItems interface, imapi.iprogressitems_progressitemfromdescription, imapi2fs/IProgressItems::ProgressItemFromDescription
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
 - IProgressItems.ProgressItemFromDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProgressItems::ProgressItemFromDescription


## -description


Retrieves a progress item based on the specified file name.


## -parameters




### -param description [in]

String that contains the file name of the progress item to retrieve. The method returns the progress item if this string matches the value for item's description property.


### -param item [out]

An <a href="https://msdn.microsoft.com/b6ba9226-655e-4eac-ad43-2b5a8e90039f">IProgressItem</a> interface of the progress item associated with the specified file name.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
<i>description</i> is <b>NULL</b>.

Value:0x80004005

</td>
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
 




## -see-also




<a href="https://msdn.microsoft.com/b6ba9226-655e-4eac-ad43-2b5a8e90039f">IProgressItem</a>



<a href="https://msdn.microsoft.com/40c28e67-8ff3-4330-90a1-7ebccb0023ad">IProgressItems</a>



<a href="https://msdn.microsoft.com/2b37cf63-24be-42ff-a439-157703db9604">IProgressItems::ProgressItemFromBlock</a>



<a href="https://msdn.microsoft.com/74d8e74d-0af6-457a-a16b-f959757b5a86">IProgressItems::get_Item</a>
 

 

