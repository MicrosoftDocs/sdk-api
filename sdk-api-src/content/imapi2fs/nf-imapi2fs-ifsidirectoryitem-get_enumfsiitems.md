---
UID: NF:imapi2fs.IFsiDirectoryItem.get_EnumFsiItems
title: IFsiDirectoryItem::get_EnumFsiItems
author: windows-sdk-content
description: Retrieves a list of child items contained within the directory in the file system image.
old-location: imapi\ifsidirectoryitem_get_enumfsiitems.htm
tech.root: imapi
ms.assetid: 723f28ad-f77d-494f-9ae6-ba6120675cfd
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IFsiDirectoryItem interface [IMAPI],get_EnumFsiItems method, IFsiDirectoryItem.get_EnumFsiItems, IFsiDirectoryItem::get_EnumFsiItems, get_EnumFsiItems, get_EnumFsiItems method [IMAPI], get_EnumFsiItems method [IMAPI],IFsiDirectoryItem interface, imapi.ifsidirectoryitem_get_enumfsiitems, imapi2fs/IFsiDirectoryItem::get_EnumFsiItems
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
 - IFsiDirectoryItem.get_EnumFsiItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2fs.h
: 
- IFsiDirectoryItem.get_EnumFsiItems
: 
---

# IFsiDirectoryItem::get_EnumFsiItems


## -description


Retrieves a list of child items contained within the directory in the file system image.


## -parameters




### -param NewEnum [out]

An <a href="https://msdn.microsoft.com/f3186af1-4056-4cb5-aac4-5253ee6dbc01">IEnumFsiItems</a> interface that contains a collection of the child directory and file items contained within the directory.


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
Failed to allocate necessary memory.

Value: 0x8007000E

</td>
</tr>
</table>
 




## -remarks



This property returns the same results as the <a href="https://msdn.microsoft.com/08ffc4dd-7001-4a89-a58e-a12e21600172">IFsiDirectoryItem::get__NewEnum</a> property and is meant for use by C/C++ applications.




## -see-also




<a href="https://msdn.microsoft.com/f3186af1-4056-4cb5-aac4-5253ee6dbc01">IEnumFsiItems</a>



<a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a>



<a href="https://msdn.microsoft.com/08ffc4dd-7001-4a89-a58e-a12e21600172">IFsiDirectoryItem::get__NewEnum</a>
 

 

