---
UID: NF:imapi2fs.IFileSystemImage.CreateDirectoryItem
title: IFileSystemImage::CreateDirectoryItem
author: windows-sdk-content
description: Create a directory item with the specified name.
old-location: imapi\ifilesystemimage_createdirectoryitem.htm
tech.root: imapi
ms.assetid: 27eadc99-46b6-40e1-91e0-b5c532536491
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CreateDirectoryItem, CreateDirectoryItem method [IMAPI], CreateDirectoryItem method [IMAPI],IFileSystemImage interface, IFileSystemImage interface [IMAPI],CreateDirectoryItem method, IFileSystemImage.CreateDirectoryItem, IFileSystemImage::CreateDirectoryItem, imapi.ifilesystemimage_createdirectoryitem, imapi2fs/IFileSystemImage::CreateDirectoryItem
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
 - IFileSystemImage.CreateDirectoryItem
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
- IFileSystemImage.CreateDirectoryItem
: 
---

# IFileSystemImage::CreateDirectoryItem


## -description


Create a directory item with the specified name.


## -parameters




### -param name [in]

String that contains the name of the directory item to create.


### -param newItem [out]

An <a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a> interface of the new directory item.  When done, call the <b>IFsiDirectoryItem::Release</b> method to release the interface.


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



After setting properties on the <a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a> interface, call the <a href="https://msdn.microsoft.com/f4855907-89e5-4127-9307-35970046a236">IFsiDirectoryItem::Add</a> method on the parent directory item to add it to the file system image.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a>
 

 

