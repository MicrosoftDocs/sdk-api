---
UID: NF:imapi2fs.DFileSystemImageImportEvents.UpdateImport
title: DFileSystemImageImportEvents::UpdateImport (imapi2fs.h)
description: Receives import notification for every file and directory item imported from an optical medium.
helpviewer_keywords: ["DFileSystemImageImportEvents interface [IMAPI]","UpdateImport method","DFileSystemImageImportEvents.UpdateImport","DFileSystemImageImportEvents::UpdateImport","UpdateImport","UpdateImport method [IMAPI]","UpdateImport method [IMAPI]","DFileSystemImageImportEvents interface","imapi.dfilesystemimageimportevents_updateimport","imapi2fs/DFileSystemImageImportEvents::UpdateImport"]
old-location: imapi\dfilesystemimageimportevents_updateimport.htm
tech.root: imapi
ms.assetid: 83617039-686d-4c03-9f43-02ecde2ca53e
ms.date: 12/05/2018
ms.keywords: DFileSystemImageImportEvents interface [IMAPI],UpdateImport method, DFileSystemImageImportEvents.UpdateImport, DFileSystemImageImportEvents::UpdateImport, UpdateImport, UpdateImport method [IMAPI], UpdateImport method [IMAPI],DFileSystemImageImportEvents interface, imapi.dfilesystemimageimportevents_updateimport, imapi2fs/DFileSystemImageImportEvents::UpdateImport
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
 - DFileSystemImageImportEvents::UpdateImport
 - imapi2fs/DFileSystemImageImportEvents::UpdateImport
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
 - DFileSystemImageImportEvents.UpdateImport
---

# DFileSystemImageImportEvents::UpdateImport


## -description

Receives import notification for every file and directory item imported from an optical medium.

## -parameters

### -param object [in]

Pointer to an <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3">IFilesystemImage3</a> interface of a file system image object to which data is being imported.

### -param fileSystem [in]

Type of the file system currently being imported. For possible values, see the <a href="/windows/desktop/api/imapi2fs/ne-imapi2fs-fsifilesystems">FsiFileSystems</a> enumeration type.

### -param currentItem [in]

A string containing the name of the file or directory being imported at the moment.

### -param importedDirectoryItems [in]

The number of directories imported so far.

### -param totalDirectoryItems [in]

The total number of directories to be imported from the optical medium.

### -param importedFileItems [in]

The number of files imported so far.

### -param totalFileItems [in]

The total number of files to be imported from the optical medium.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Notifications are sent in response to calling one of the following methods for importing a file system.

<ul>
<li>
<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem">IFileSystemImage::ImportFileSystem</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem">IFileSystemImage::ImportSpecificFileSystem</a>
</li>
</ul>
UpdateImport method receives import notifications from ISO9660, Joliet and UDF file systems. A notification is sent:

<ul>
<li>Once after every individual imported file.</li>
<li>Once before every directory import begins.</li>
</ul>
The <i>totalFileItems</i> parameter of an <b>UpdateImport</b> event is always set to (-1) for ISO9660 and Joliet file systems, because of the difficulty quickly and accurately determining the total number of files in an ISO9660/Joliet file system prior to import.

Import notifications are generated only for files and directories, and not for associated named streams.

If the <i>currentItem</i> is a directory, it contains a back slash '\' at the end.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents">DFileSystemImageImportEvents</a>