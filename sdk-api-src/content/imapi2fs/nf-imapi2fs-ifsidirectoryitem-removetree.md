---
UID: NF:imapi2fs.IFsiDirectoryItem.RemoveTree
title: IFsiDirectoryItem::RemoveTree
author: windows-sdk-content
description: Remove the specified directory tree from the file system image.
old-location: imapi\ifsidirectoryitem_removetree.htm
old-project: imapi
ms.assetid: d0aad985-306c-41a2-9711-9265a4f492c5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IFsiDirectoryItem interface [IMAPI],RemoveTree method, IFsiDirectoryItem.RemoveTree, IFsiDirectoryItem::RemoveTree, RemoveTree, RemoveTree method [IMAPI], RemoveTree method [IMAPI],IFsiDirectoryItem interface, imapi.ifsidirectoryitem_removetree, imapi2fs/IFsiDirectoryItem::RemoveTree
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi2fs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PlatformId
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFsiDirectoryItem.RemoveTree
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFsiDirectoryItem::RemoveTree


## -description


Remove the specified directory tree from the file system image.


## -parameters




### -param path [in]

String that contains the name of directory to remove.
The path is relative to current directory item.


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
The <i>path</i> parameter is not a valid pointer.

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
<dt><b>	IMAPI_E_NOT_IN_FILE_SYSTEM</b></dt>
</dl>
</td>
<td width="60%">
<i>ls!'</i> is not part of the file system. It must be added to complete this operation.

Value: 0xC0AAB10B

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
FileSystemImage object is in read only mode.

Value: 0xC0AAB102

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_DIR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified directory does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_DIR_NOT_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The directory <i>%1!s!</i> is not empty.

Value: 0xC0AAB10A

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_FSI_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Internal error occurred: <i>%1!ls!</i>.

Value: 0xC0AAB100

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_NOT_DIR</b></dt>
</dl>
</td>
<td width="60%">
Specified path <i>%1!ls!</i> does not identify a directory.

Value: 0xC0AAB109

</td>
</tr>
</table>
 




## -remarks



The directory item must be  present in the file system image.


You can delete the entire file-system image by calling this method for the root directory item and setting the path to a single path delimiter (\).




## -see-also




<a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a>



<a href="https://msdn.microsoft.com/bb716e60-163c-45e7-bdbb-373666cbdc93">IFsiDirectoryItem::AddDirectory</a>



<a href="https://msdn.microsoft.com/82f62372-3c79-4bf5-a723-cd09a5444ffc">IFsiDirectoryItem::AddFile</a>



<a href="https://msdn.microsoft.com/4f36538c-fba7-4a0c-a2e9-443b7dc2fdab">IFsiDirectoryItem::AddTree</a>



<a href="https://msdn.microsoft.com/bbd45185-439a-4847-8481-7139e81b34fd">IFsiDirectoryItem::Remove</a>
 

 

