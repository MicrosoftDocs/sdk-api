---
UID: NN:imapi2fs.IFsiDirectoryItem
title: IFsiDirectoryItem
author: windows-sdk-content
description: Use this interface to add items to or remove items from the file-system image.
old-location: imapi\ifsidirectoryitem.htm
tech.root: imapi
ms.assetid: 1c9a2e36-0e79-4bad-b880-ddfbf473308b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFsiDirectoryItem, IFsiDirectoryItem interface [IMAPI], IFsiDirectoryItem interface [IMAPI],described, imapi.ifsidirectoryitem, imapi2fs/IFsiDirectoryItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IFsiDirectoryItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsiDirectoryItem interface


## -description


Use this interface to add items to or remove items from the file-system image. 

To get this interface, call the <a href="https://msdn.microsoft.com/27eadc99-46b6-40e1-91e0-b5c532536491">IFileSystemImage::CreateDirectoryItem</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsiDirectoryItem</b> interface inherits from <a href="https://msdn.microsoft.com/44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0">IFsiItem</a>. <b>IFsiDirectoryItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsiDirectoryItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4855907-89e5-4127-9307-35970046a236">Add</a>
</td>
<td align="left" width="63%">
Adds a file or directory described by the FsiItem object to the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb716e60-163c-45e7-bdbb-373666cbdc93">AddDirectory</a>
</td>
<td align="left" width="63%">
Adds a directory to the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82f62372-3c79-4bf5-a723-cd09a5444ffc">AddFile</a>
</td>
<td align="left" width="63%">
Adds a file to the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f36538c-fba7-4a0c-a2e9-443b7dc2fdab">AddTree</a>
</td>
<td align="left" width="63%">
Adds the contents of a directory tree to the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08ffc4dd-7001-4a89-a58e-a12e21600172">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves a list of child items contained within the directory in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66553025-35c9-4902-a184-01c07a478977">get_Count</a>
</td>
<td align="left" width="63%">
Number of  child items in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/723f28ad-f77d-494f-9ae6-ba6120675cfd">get_EnumFsiItems</a>
</td>
<td align="left" width="63%">
Retrieves a list of child items contained within the directory in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ea5219c-a12f-43a3-a67b-16cd0e6d2bac">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the specified directory or file item from file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbd45185-439a-4847-8481-7139e81b34fd">Remove</a>
</td>
<td align="left" width="63%">
Removes the specified item from the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0aad985-306c-41a2-9711-9265a4f492c5">RemoveTree</a>
</td>
<td align="left" width="63%">
Remove the specified directory tree from the file system image.

</td>
</tr>
</table> 


## -remarks



Each directory item contains an enumerable collection of child items within the directory.

You can add and remove files and directories only after the directory item has been added to the file system image.


This is an <b>FsiDirectoryItem</b> object in script.




## -see-also




<a href="https://msdn.microsoft.com/27eadc99-46b6-40e1-91e0-b5c532536491">IFileSystemImage::CreateDirectoryItem</a>



<a href="https://msdn.microsoft.com/44494e66-e6b4-4acb-a2a6-0a3e5cc4a2a0">IFsiItem</a>
 

 

