---
UID: NF:imapi2fs.DFileSystemImageEvents.Update
title: DFileSystemImageEvents::Update (imapi2fs.h)
description: Implement this method to receive progress notification of the current write operation. The notifications are sent when copying the content of a file or while adding directories or files to the file system image.
helpviewer_keywords: ["DFileSystemImageEvents interface [IMAPI]","Update method","DFileSystemImageEvents.Update","DFileSystemImageEvents::Update","Update","Update method [IMAPI]","Update method [IMAPI]","DFileSystemImageEvents interface","imapi.dfilesystemimageevents_update","imapi2fs/DFileSystemImageEvents::Update"]
old-location: imapi\dfilesystemimageevents_update.htm
tech.root: imapi
ms.assetid: 7d639391-77ee-4889-a11b-1bbd1b88b38e
ms.date: 12/05/2018
ms.keywords: DFileSystemImageEvents interface [IMAPI],Update method, DFileSystemImageEvents.Update, DFileSystemImageEvents::Update, Update, Update method [IMAPI], Update method [IMAPI],DFileSystemImageEvents interface, imapi.dfilesystemimageevents_update, imapi2fs/DFileSystemImageEvents::Update
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - DFileSystemImageEvents::Update
 - imapi2fs/DFileSystemImageEvents::Update
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
 - DFileSystemImageEvents.Update
---

# DFileSystemImageEvents::Update


## -description

Implement this method to receive progress notification of the current write operation. The notifications are sent when copying the content of a file or while adding directories or files to the file system image.

## -parameters

### -param object [in]

An <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a> interface of the file system image that is being written. 

This parameter is a <b>CFileSystemImage</b> object in a script.

### -param currentFile [in]

String that contains the full path of the file being written.

### -param copiedSectors [in]

Number of sectors copied.

### -param totalSectors [out]

Total number of sectors in the file.

## -returns

Return values are ignored.

## -remarks

Notifications are sent in response to calling one of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-add">IFsiDirectoryItem::Add</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addfile">IFsiDirectoryItem::AddFile</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree">IFsiDirectoryItem::AddTree</a>
</li>
</ul>
Notifications can also be sent when calling one of the following methods to import a UDF file system that was created using immediate allocation (immediate allocation means that the file data is contained within the file descriptor instead of having allocation descriptors in the file descriptor that point to sectors of data):

<ul>
<li>
<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem">IFileSystemImage::ImportFileSystem</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem">IFileSystemImage::ImportSpecificFileSystem</a>
</li>
</ul>
Notification is sent:

<ul>
<li>Once before adding the first sector of a file (<i>copiedSectors</i> is 0)</li>
<li>For every megabyte that is written</li>
<li>Once after the final write if the file did not end on a megabyte boundary</li>
</ul>

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents">DFileSystemImageEvents</a>