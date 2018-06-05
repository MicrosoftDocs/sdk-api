---
UID: NF:vds.IVdsVolumeMF.AddAccessPath
title: IVdsVolumeMF::AddAccessPath
author: windows-sdk-content
description: Adds an access path.
old-location: base\ivdsvolumemf_addaccesspath.htm
old-project: VDS
ms.assetid: cf29639e-33fd-42f6-b616-7145521da347
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: AddAccessPath, AddAccessPath method [VDS], AddAccessPath method [VDS],IVdsVolumeMF interface, IVdsVolumeMF interface [VDS],AddAccessPath method, IVdsVolumeMF.AddAccessPath, IVdsVolumeMF::AddAccessPath, base.ivdsvolumemf_addaccesspath, vds/IVdsVolumeMF::AddAccessPath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsVolumeMF.AddAccessPath
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolumeMF::AddAccessPath


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Adds an 
   access path.


## -parameters




### -param pwszPath [in]

A string indicating the access path, which is a user-mode path that can be used to open the volume. An access path can be a drive letter or a path to an empty directory on an NTFS volume. The access path string must include a trailing 
      backslash, for example, "F:\".


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The path was added successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The access path was added successfully, however, an error occurred. VDS possibly failed to update the 
        GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER attribute of a partition or failed to add a default network share (such as F$) 
        while adding the drive letter. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563763">PARTITION_INFORMATION_GPT</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The volume failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PACK_OFFLINE</b></dt>
<dt>0x80042444L</dt>
</dl>
</td>
<td width="60%">
The pack containing the volume is not accessible.

</td>
</tr>
</table>
 




## -remarks



VDS adds the access path by creating a mounted folder (also called a volume mount point). Note that mounted folders are supported only on NTFS volumes. For more information, see <a href="https://msdn.microsoft.com/6de526cd-5537-4411-b43f-3c0bdac70d64">Mounted Folders</a>.

This method returns ERROR_DIR_NOT_EMPTY if the <i>pwszPath</i> parameter contains a path to a mounted folder that is already in use (even if the directory is empty) or if <i>pwszPath</i> contains a path to a nonempty directory. 




## -see-also




<a href="https://msdn.microsoft.com/4c8a63bd-ae2f-4157-92f9-aefc592c7d4f">IVdsVolumeMF</a>



<a href="https://msdn.microsoft.com/1535fe64-221a-4756-a9ba-81bbe7596598">SetVolumeMountPoint</a>
 

 

