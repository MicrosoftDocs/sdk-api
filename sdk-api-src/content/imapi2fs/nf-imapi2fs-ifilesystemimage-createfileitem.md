---
UID: NF:imapi2fs.IFileSystemImage.CreateFileItem
title: IFileSystemImage::CreateFileItem
author: windows-sdk-content
description: Create a file item with the specified name.
old-location: imapi\ifilesystemimage_createfileitem.htm
tech.root: imapi
ms.assetid: 8e90e367-e7c3-41db-a8c9-9b0220cf402b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateFileItem, CreateFileItem method [IMAPI], CreateFileItem method [IMAPI],IFileSystemImage interface, IFileSystemImage interface [IMAPI],CreateFileItem method, IFileSystemImage.CreateFileItem, IFileSystemImage::CreateFileItem, imapi.ifilesystemimage_createfileitem, imapi2fs/IFileSystemImage::CreateFileItem
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
 - IFileSystemImage.CreateFileItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemImage::CreateFileItem


## -description


Create a file item with the specified name.


## -parameters




### -param name [in]

String that contains the name of the file item to create.


### -param newItem [out]

An <a href="https://msdn.microsoft.com/13085b1f-4ff9-48ff-a9ae-9a1c5cb9a108">IFsiFileItem</a> interface of the new file item.  When done, call the <b>IFsiFileItem::Release</b> method to release the interface.


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
The provided <i>name</i>  is not valid.

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



After setting properties on the <a href="https://msdn.microsoft.com/13085b1f-4ff9-48ff-a9ae-9a1c5cb9a108">IFsiFileItem</a> interface, call the <a href="https://msdn.microsoft.com/f4855907-89e5-4127-9307-35970046a236">IFsiDirectoryItem::Add</a> method on the parent directory item to add it to the file system image.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/13085b1f-4ff9-48ff-a9ae-9a1c5cb9a108">IFsiFileItem</a>
 

 

