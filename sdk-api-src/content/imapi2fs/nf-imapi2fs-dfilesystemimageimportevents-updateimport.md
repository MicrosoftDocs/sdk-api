---
UID: NF:imapi2fs.DFileSystemImageImportEvents.UpdateImport
title: DFileSystemImageImportEvents::UpdateImport
author: windows-driver-content
description: Receives import notification for every file and directory item imported from an optical medium.
old-location: imapi\dfilesystemimageimportevents_updateimport.htm
old-project: imapi
ms.assetid: 83617039-686d-4c03-9f43-02ecde2ca53e
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: DFileSystemImageImportEvents interface [IMAPI],UpdateImport method, DFileSystemImageImportEvents.UpdateImport, DFileSystemImageImportEvents::UpdateImport, UpdateImport, UpdateImport method [IMAPI], UpdateImport method [IMAPI],DFileSystemImageImportEvents interface, imapi.dfilesystemimageimportevents_updateimport, imapi2fs/DFileSystemImageImportEvents::UpdateImport
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
-	DFileSystemImageImportEvents.UpdateImport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# DFileSystemImageImportEvents::UpdateImport


## -description


Receives import notification for every file and directory item imported from an optical medium.


## -parameters




### -param object [in]

Pointer to an <a href="https://msdn.microsoft.com/ffe343fa-2837-41f7-b7e0-097788fb5d4e">IFilesystemImage3</a> interface of a file system image object to which data is being imported.


### -param fileSystem [in]

Type of the file system currently being imported. For possible values, see the <a href="https://msdn.microsoft.com/afb27235-a9b4-4629-aac0-9c43e5b2cf3f">FsiFileSystems</a> enumeration type.


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Notifications are sent in response to calling one of the following methods for importing a file system.

<ul>
<li>
<a href="https://msdn.microsoft.com/87d654bc-f2c9-4a74-a822-352cdb242b5f">IFileSystemImage::ImportFileSystem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/737f1b5a-be70-4869-9ad0-a1373cb865d9">IFileSystemImage::ImportSpecificFileSystem</a>
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




<a href="https://msdn.microsoft.com/972ab985-17c5-4458-a7f4-59ac25c0dca4">DFileSystemImageImportEvents</a>
 

 

