---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

