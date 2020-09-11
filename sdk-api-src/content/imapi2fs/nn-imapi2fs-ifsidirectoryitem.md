---
UID: NN:imapi2fs.IFsiDirectoryItem
title: IFsiDirectoryItem (imapi2fs.h)
description: Use this interface to add items to or remove items from the file-system image.
helpviewer_keywords: ["IFsiDirectoryItem","IFsiDirectoryItem interface [IMAPI]","IFsiDirectoryItem interface [IMAPI]","described","imapi.ifsidirectoryitem","imapi2fs/IFsiDirectoryItem"]
old-location: imapi\ifsidirectoryitem.htm
tech.root: imapi
ms.assetid: 1c9a2e36-0e79-4bad-b880-ddfbf473308b
ms.date: 12/05/2018
ms.keywords: IFsiDirectoryItem, IFsiDirectoryItem interface [IMAPI], IFsiDirectoryItem interface [IMAPI],described, imapi.ifsidirectoryitem, imapi2fs/IFsiDirectoryItem
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsiDirectoryItem
 - imapi2fs/IFsiDirectoryItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFsiDirectoryItem
---

# IFsiDirectoryItem interface


## -description

Use this interface to add items to or remove items from the file-system image. 

To get this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem">IFileSystemImage::CreateDirectoryItem</a> method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsiDirectoryItem</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a>. <b>IFsiDirectoryItem</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-add">Add</a>
</td>
<td align="left" width="63%">
Adds a file or directory described by the FsiItem object to the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-adddirectory">AddDirectory</a>
</td>
<td align="left" width="63%">
Adds a directory to the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addfile">AddFile</a>
</td>
<td align="left" width="63%">
Adds a file to the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree">AddTree</a>
</td>
<td align="left" width="63%">
Adds the contents of a directory tree to the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves a list of child items contained within the directory in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Number of  child items in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-get_enumfsiitems">get_EnumFsiItems</a>
</td>
<td align="left" width="63%">
Retrieves a list of child items contained within the directory in the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves the specified directory or file item from file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes the specified item from the file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree">RemoveTree</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem">IFileSystemImage::CreateDirectoryItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a>

