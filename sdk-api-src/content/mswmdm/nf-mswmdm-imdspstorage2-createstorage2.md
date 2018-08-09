---
UID: NF:mswmdm.IMDSPStorage2.CreateStorage2
title: IMDSPStorage2::CreateStorage2
author: windows-sdk-content
description: The CreateStorage2 method creates a new storage with the specified name and returns a pointer to the IMDSPStorage interface on the newly created storage.
old-location: wmdm\imdspstorage2_createstorage2.htm
old-project: WMDM
ms.assetid: f79f4bf5-948e-4201-a9bc-edde4dd333ea
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateStorage2, CreateStorage2 method [windows Media Device Manager], CreateStorage2 method [windows Media Device Manager],IMDSPStorage2 interface, IMDSPStorage2 interface [windows Media Device Manager],CreateStorage2 method, IMDSPStorage2.CreateStorage2, IMDSPStorage2::CreateStorage2, IMDSPStorage2CreateStorage2, mswmdm/IMDSPStorage2::CreateStorage2, wmdm.imdspstorage2_createstorage2
ms.prod: windows
ms.technology: windows-sdk
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
 - IMDSPStorage2.CreateStorage2
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPStorage2::CreateStorage2


## -description



The <b>CreateStorage2</b> method creates a new storage with the specified name and returns a pointer to the <b>IMDSPStorage</b> interface on the newly created storage.




## -parameters




### -param dwAttributes [in]

<b>DWORD</b> containing the attributes as described in the <b>IMDSPStorage::CreateStorage</b> method.


### -param dwAttributesEx [in]

<b>DWORD</b> containing the extended attributes. There are currently no extended attributes defined.


### -param pAudioFormat [in]

Pointer to a <b>_WAVEFORMATEX</b> structure that contains audio format information about the object. This parameter is optional and is ignored if the file is not audio.


### -param pVideoFormat [in]

Pointer to a <b>_VIDEOINFOHEADER</b> structure that contains video format information about the object. This parameter is optional and is ignored if the file is not video.


### -param pwszName [in]

Pointer to a wide-character null-terminated string containing the name for the new storage.


### -param qwFileSize [in]

<b>QWORD</b> containing the size of the file to create. If the total size of the output file is not known at the time of creation, this value will be set to zero.


### -param ppNewStorage [out]

Pointer to an <b>IMDSPStorage</b> pointer to receive the <b>IMDSPStorage</b> interface for the newly created storage.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



If both the WMDM_FILE_ATTR_FOLDER and WMDM_FILE_ATTR_FILE attributes are set, the folder attribute overrides the file attribute, and the new storage is created as a folder.

Only one of WMDM_STORAGECONTROL_INSERTBEFORE, WMDM_STORAGECONTROL_INSERTAFTER, and WMDM_STORAGECONTROL_INSERTINTO can be specified by the client.

The new storage can be created at the same level or can be inserted into the current storage, provided that the current storage is a folder. This is controlled by the value of the <i>dwAttributes</i> parameter. If it specifies WMDM_STORAGECONTROL_INSERTBEFORE or WMDM_STORAGECONTROL_INSERTAFTER, the new storage will be created at the same level as the current storage. If it specifies WMDM_STORAGECONTROL_INSERTINTO, the new storage will be inserted into the current storage.

WMDM_STORAGECONTROL_INSERTBEFORE and WMDM_STORAGECONTROL_INSERAFTER imply an ordering of content in the file system. If the file system does not support ordering (for example, FAT32) both the flags have the identical effect of inserting the new storage at the same level as the current storage. If the current storage represents the root of the storage medium, and one of these two flags is specified, the operation fails.

WMDM_STORAGECONTROL_INSERTINTO is valid only if the current storage is a folder. If the current storage is a file, and this flag is specified, the operation fails.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/39afb282-7141-4eb5-93e9-a69bef495d80">IMDSPStorage2 Interface</a>



<a href="https://msdn.microsoft.com/95633bc4-44fc-4ac7-9492-f99069d77d4d">IMDSPStorage::CreateStorage</a>
 

 

