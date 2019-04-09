---
UID: NF:mswmdm.IMDSPStorage4.CreateStorageWithMetadata
title: IMDSPStorage4::CreateStorageWithMetadata (mswmdm.h)
author: windows-sdk-content
description: The CreateStorageWithMetadata method creates a new storage, applying the given metadata to the new storage, and returns a pointer to the IMDSPStorage interface on the newly created storage.
old-location: wmdm\imdspstorage4_createstoragewithmetadata.htm
tech.root: WMDM
ms.assetid: 493eb6f1-fc06-4b37-803f-a81219e9f819
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateStorageWithMetadata, CreateStorageWithMetadata method [windows Media Device Manager], CreateStorageWithMetadata method [windows Media Device Manager],IMDSPStorage4 interface, IMDSPStorage4 interface [windows Media Device Manager],CreateStorageWithMetadata method, IMDSPStorage4.CreateStorageWithMetadata, IMDSPStorage4::CreateStorageWithMetadata, IMDSPStorage4CreateStorageWithMetadata, mswmdm/IMDSPStorage4::CreateStorageWithMetadata, wmdm.imdspstorage4_createstoragewithmetadata
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPStorage4.CreateStorageWithMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPStorage4::CreateStorageWithMetadata


## -description



The <b>CreateStorageWithMetadata</b> method creates a new storage, applying the given metadata to the new storage, and returns a pointer to the <b>IMDSPStorage</b> interface on the newly created storage. The new storage can be created at the same level or can be inserted into the current storage.



This method is useful if the device needs metadata at creation time. Depending upon the device it may also be more efficient to applying metadata at creation time as opposed to creating the storage and then setting metadata.


## -parameters




### -param dwAttributes [in]

<b>DWORD</b> containing attributes for the new storage. The following table lists the available storage attributes.

<table>
<tr>
<th>Attribute
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_STORAGECONTROL_INSERTBEFORE</td>
<td>The new storage object will be created in front of the target object.</td>
</tr>
<tr>
<td>WMDM_STORAGECONTROL_INSERTAFTER</td>
<td>The new storage object will be created after the target object.</td>
</tr>
<tr>
<td>WMDM_STORAGECONTROL_INSERTINTO</td>
<td>The new storage object will be created in the target object folder.</td>
</tr>
<tr>
<td>WMDM_STORAGECONTROL_OVERWRITE</td>
<td>If storage with the same name already exists, it will be destroyed and a new storage created.</td>
</tr>
<tr>
<td>WMDM_STORAGE_ATTR_FILESYSTEM</td>
<td>This object is the top-level storage medium (for example, a storage card or some other onboard storage.)</td>
</tr>
<tr>
<td>WMDM_STORAGE_ATTR_REMOVABLE</td>
<td>This storage medium is removable.</td>
</tr>
<tr>
<td>WMDM_STORAGE_ATTR_CANEDITMETADATA</td>
<td>This storage can edit metadata.</td>
</tr>
<tr>
<td>WMDM_STORAGE_ATTR_FOLDERS</td>
<td>This storage medium supports folders and file hierarchy.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_FOLDER</td>
<td>This is a folder on the storage medium.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_LINK</td>
<td>This is a link that creates an association among multiple files.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_FILE</td>
<td>This is a file on the storage medium.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_AUDIO</td>
<td>This file is audio data.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_DATA</td>
<td>This file is non-audio data.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_CANPLAY</td>
<td>This audio file can be played by the device.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_CANDELETE</td>
<td>This file can be deleted.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_CANMOVE</td>
<td>This file or folder can be moved on the storage medium.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_CANRENAME</td>
<td>This file or folder can be renamed.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_CANREAD</td>
<td>This file can be read by the host computer.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_MUSIC</td>
<td>This audio file is music.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_PLAYLIST</td>
<td>This is a playlist object.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_VIDEO</td>
<td>This file contains video data.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_HIDDEN</td>
<td>This file is hidden on the file system.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_SYSTEM</td>
<td>This is a system file.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_READONLY</td>
<td>This is a read-only file.</td>
</tr>
<tr>
<td>WMDM_STORAGE_IS_DEFAULT</td>
<td>This storage is the default storage where new media should be placed.</td>
</tr>
<tr>
<td>WMDM_STORAGE_CONTAINS_DEFAULT</td>
<td>This storage contains the default storage where new media should be placed.</td>
</tr>
</table>
 


### -param pwszName [in]

Pointer to a wide-character, null-terminated string containing a name for the new storage.


### -param pMetadata [in]

Pointer to an <b>IWMDMMetaData</b> interface.


### -param qwFileSize [in]

<b>Qword</b> containing the file size.


### -param ppNewStorage [out]

Pointer to an <b>IMDSPStorage</b> pointer to receive the <b>IMDSPStorage</b> interface for the newly created storage.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



This method is useful if metadata needs to be applied to storage at the creation time. In contrast, the <b>IMDSPStorage2::CreateStorage2</b> and <b>IMDSPStorage::CreateStorage</b> methods do not provide a way for supplying metadata at creation time.

If service provider for a device that can synchronize with Windows Media Player supports this interface, Windows Media Device Manager calls this method during <a href="https://msdn.microsoft.com/909b94fd-99de-4e26-87d6-d074a6eb5da3">Insert</a>/2/3 operations.

If both the WMDM_FILE_ATTR_FOLDER and WMDM_FILE_ATTR_FILE attributes are set, the folder attribute overrides the file attribute, and the new storage is created as a folder.

Only one of WMDM_STORAGECONTROL_INSERTBEFORE, WMDM_STORAGECONTROL_INSERTAFTER, and WMDM_STORAGECONTROL_INSERTINTO can be specified by the client.

The new storage can be created at the same level or can be inserted into the current storage provided that the current storage is a folder. This is controlled by the value of <i>dwAttributes</i> parameter. If it specifies WMDM_STORAGECONTROL_INSERTBEFORE or WMDM_STORAGECONTROL_INSERTAFTER, the new storage will be created at the same level as the current storage. If it specifies WMDM_STORAGECONTROL_INSERTINTO, the new storage will be inserted into the current storage.

WMDM_STORAGECONTROL_INSERTBEFORE and WMDM_STORAGECONTROL_INSERAFTER imply an ordering of content in the file system. If the file system does not support ordering (for example, the FAT32 file system), both flags have the identical effect of inserting the new storage at the level of the current storage. If the current storage represents the root of the storage medium and one of these two flags is specified, the operation fails.

WMDM_STORAGECONTROL_INSERTINTO is valid only if the current storage is a folder. If the current storage is a file and this flag is specified, the operation fails.




## -see-also




<a href="https://msdn.microsoft.com/a312dfef-ac48-4c58-a59a-b277f5386419">Enabling Synchronization with Windows Media Player</a>



<a href="https://msdn.microsoft.com/f79f4bf5-948e-4201-a9bc-edde4dd333ea">IMDSPStorage2::CreateStorage2</a>



<a href="https://msdn.microsoft.com/c1236acc-1f11-4501-9374-2486f7d61db3">IMDSPStorage4 Interface</a>



<a href="https://msdn.microsoft.com/95633bc4-44fc-4ac7-9492-f99069d77d4d">IMDSPStorage::CreateStorage</a>
 

 

