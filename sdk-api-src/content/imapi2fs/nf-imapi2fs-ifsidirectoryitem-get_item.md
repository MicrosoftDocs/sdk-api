---
UID: NF:imapi2fs.IFsiDirectoryItem.get_Item
title: IFsiDirectoryItem::get_Item
author: windows-driver-content
description: Retrieves the specified directory or file item from file system image.
old-location: imapi\ifsidirectoryitem_get_item.htm
old-project: imapi
ms.assetid: 8ea5219c-a12f-43a3-a67b-16cd0e6d2bac
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: IFsiDirectoryItem interface [IMAPI],get_Item method, IFsiDirectoryItem.get_Item, IFsiDirectoryItem::get_Item, get_Item, get_Item method [IMAPI], get_Item method [IMAPI],IFsiDirectoryItem interface, imapi.ifsidirectoryitem_get_item, imapi2fs/IFsiDirectoryItem::get_Item
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
-	IFsiDirectoryItem.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFsiDirectoryItem::get_Item


## -description


Retrieves the specified directory or file item from file system image.


## -parameters




### -param path [in]

String that contains the path to the item to retrieve.


### -param item [out]

An <a href="https://msdn.microsoft.com/44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0">IFsiItem</a> interface of the requested directory or file item.


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
<dt><b>IMAPI_E_INVALID_PATH</b></dt>
</dl>
</td>
<td width="60%">
Path '%1!s!' is badly formed or contains invalid characters.

Value: 0xC0AAB110

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
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The value specified for parameter <i>%1!ls!</i> is not valid.

Value: 0xC0AAB101

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_ITEM_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Cannot find item <i>%1!ls!</i> in FileSystemImage hierarchy.

Value: 0xC0AAB118

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



To determine whether the item is a file item or directory item, call the <a href="https://msdn.microsoft.com/44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0">IFsiItem::QueryInterface</a>  method passing __uuidof(IFsiDirectoryItem) as the interface identifier. If the call succeeds, the item is a directory item; otherwise, the item is a file item.

To enumerate all children, call the <a href="https://msdn.microsoft.com/08ffc4dd-7001-4a89-a58e-a12e21600172">IFsiDirectoryItem::get__NewEnum</a> method.




## -see-also




<a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a>



IFsiFileItem
 

 

