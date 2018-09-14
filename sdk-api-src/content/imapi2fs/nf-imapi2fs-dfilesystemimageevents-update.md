---
UID: NF:imapi2fs.DFileSystemImageEvents.Update
title: DFileSystemImageEvents::Update
author: windows-sdk-content
description: Implement this method to receive progress notification of the current write operation. The notifications are sent when copying the content of a file or while adding directories or files to the file system image.
old-location: imapi\dfilesystemimageevents_update.htm
tech.root: imapi
ms.assetid: 7d639391-77ee-4889-a11b-1bbd1b88b38e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DFileSystemImageEvents interface [IMAPI],Update method, DFileSystemImageEvents.Update, DFileSystemImageEvents::Update, Update, Update method [IMAPI], Update method [IMAPI],DFileSystemImageEvents interface, imapi.dfilesystemimageevents_update, imapi2fs/DFileSystemImageEvents::Update
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
req.idl: Imapi2.idl
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
 - DFileSystemImageEvents.Update
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DFileSystemImageEvents::Update


## -description


Implement this method to receive progress notification of the current write operation. The notifications are sent when copying the content of a file or while adding directories or files to the file system image.


## -parameters




### -param object

TBD


### -param currentFile [in]

String that contains the full path of the file being written.


### -param copiedSectors [in]

Number of sectors copied.


### -param totalSectors [out]

Total number of sectors in the file.


#### - fileSystemImage [in]

An <a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a> interface of the file system image that is being written. 

This parameter is a <b>CFileSystemImage</b> object in a script.


## -returns



Return values are ignored.




## -remarks



Notifications are sent in response to calling one of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/f4855907-89e5-4127-9307-35970046a236">IFsiDirectoryItem::Add</a>
</li>
<li>
<a href="https://msdn.microsoft.com/82f62372-3c79-4bf5-a723-cd09a5444ffc">IFsiDirectoryItem::AddFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4f36538c-fba7-4a0c-a2e9-443b7dc2fdab">IFsiDirectoryItem::AddTree</a>
</li>
</ul>
Notifications can also be sent when calling one of the following methods to import a UDF file system that was created using immediate allocation (immediate allocation means that the file data is contained within the file descriptor instead of having allocation descriptors in the file descriptor that point to sectors of data):

<ul>
<li>
<a href="https://msdn.microsoft.com/87d654bc-f2c9-4a74-a822-352cdb242b5f">IFileSystemImage::ImportFileSystem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/737f1b5a-be70-4869-9ad0-a1373cb865d9">IFileSystemImage::ImportSpecificFileSystem</a>
</li>
</ul>
Notification is sent:

<ul>
<li>Once before adding the first sector of a file (<i>copiedSectors</i> is 0)</li>
<li>For every megabyte that is written</li>
<li>Once after the final write if the file did not end on a megabyte boundary</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/cff27ceb-d14a-48c2-941e-d27d6505e2c5">DFileSystemImageEvents</a>
 

 

