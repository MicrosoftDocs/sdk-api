---
UID: NF:mswmdm.IWMDMStorage.GetAttributes
title: IWMDMStorage::GetAttributes
author: windows-sdk-content
description: The GetAttributes method retrieves the attributes of the storage.
old-location: wmdm\iwmdmstorage_getattributes.htm
old-project: WMDM
ms.assetid: e43139d2-260a-4f27-a06c-aca741204663
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetAttributes, GetAttributes method [windows Media Device Manager], GetAttributes method [windows Media Device Manager],IWMDMStorage interface, IWMDMStorage interface [windows Media Device Manager],GetAttributes method, IWMDMStorage.GetAttributes, IWMDMStorage::GetAttributes, IWMDMStorageGetAttributes, mswmdm/IWMDMStorage::GetAttributes, wmdm.iwmdmstorage_getattributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMStorage.GetAttributes
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorage::GetAttributes


## -description



The <b>GetAttributes</b> method retrieves the attributes of the storage.




## -parameters




### -param pdwAttributes [out]

Pointer to a <b>DWORD</b> specifying one or more of the following attributes, combined with a bitwise <b>OR</b>.

<table>
<tr>
<th>Attribute
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_STORAGE_ATTR_FILESYSTEM</td>
<td>This object is the top-level storage medium, for example, a storage card or some other type of on-board storage.</td>
</tr>
<tr>
<td>WMDM_STORAGE_ATTR_REMOVABLE</td>
<td>The global storage medium is removable.</td>
</tr>
<tr>
<td>WMDM_STORAGE_ATTR_NONREMOVABLE</td>
<td>The global storage medium is not removable.</td>
</tr>
<tr>
<td>WMDM_STORAGE_ATTR_FOLDERS</td>
<td>The global storage medium supports folders and file hierarchy.</td>
</tr>
<tr>
<td>WMDM_STORAGE_ATTR_HAS_FILES</td>
<td>This storage object contains at least one file as an immediate child.</td>
</tr>
<tr>
<td>WMDM_STORAGE_ATTR_HAS_FOLDERS</td>
<td>This storage object contains at least one folder as an immediate child.</td>
</tr>
<tr>
<td>WMDM_STORAGE_ATTR_CANEDITMETADATA</td>
<td>This storage can edit metadata.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_FILE</td>
<td>This is a file on the storage medium.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_FOLDER</td>
<td>This is a folder on the storage medium.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_LINK</td>
<td>This is a link that creates an association between multiple files.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_AUDIO</td>
<td>This file contains audio data.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_DATA</td>
<td>This file contains non-audio data.</td>
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
<td>This file or folder can be moved around on the storage medium.</td>
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
<td>This audio file contains music.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_AUDIOBOOK</td>
<td>This is an audio book file.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_VIDEO</td>
<td>This file contains video data.</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_HIDDEN</td>
<td>This file is hidden on the file system</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_SYSTEM</td>
<td>This is a system file</td>
</tr>
<tr>
<td>WMDM_FILE_ATTR_READONLY</td>
<td>This is a read-only file.</td>
</tr>
<tr>
<td>WMDM_STORAGE_ATTR_VIRTUAL</td>
<td>This storage is virtual and does not correspond to an actual storage on the file system of the device. (Folders created based on metadata are one example of virtual storage.)</td>
</tr>
<tr>
<td>WMDM_STORAGE_IS_DEFAULT</td>
<td>This storage is the default location for putting new digital media on the device.</td>
</tr>
<tr>
<td>WMDM_STORAGE_CONTAINS_DEFAULT</td>
<td>This storage contains the default storage where new digital media should be placed.</td>
</tr>
</table>
 


### -param pFormat [out]

Optional pointer to a <a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a> structure that specifies the object's audio attributes.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0">Exploring a Device</a>



<a href="https://msdn.microsoft.com/6ea80ab2-718b-464e-a805-9910460931bb">IWMDMEnumStorage Interface</a>



<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>



<a href="https://msdn.microsoft.com/ab3c6a17-5a86-419b-b528-fd0db718de8f">IWMDMStorage::EnumStorage</a>



<a href="https://msdn.microsoft.com/7484e29a-5faf-4a11-9fc1-75aa5c9d72ef">IWMDMStorage::SetAttributes</a>



<a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_WAVEFORMATEX</a>
 

 

