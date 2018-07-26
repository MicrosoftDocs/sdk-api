---
UID: NF:vds.IVdsVolumeMF.DeleteAccessPath
title: IVdsVolumeMF::DeleteAccessPath
author: windows-sdk-content
description: Removes the access path from the current volume.
old-location: base\ivdsvolumemf_deleteaccesspath.htm
old-project: vds
ms.assetid: 05020390-475f-4528-ba44-ecdfe008149f
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: DeleteAccessPath, DeleteAccessPath method [VDS], DeleteAccessPath method [VDS],IVdsVolumeMF interface, IVdsVolumeMF interface [VDS],DeleteAccessPath method, IVdsVolumeMF.DeleteAccessPath, IVdsVolumeMF::DeleteAccessPath, base.ivdsvolumemf_deleteaccesspath, vds/IVdsVolumeMF::DeleteAccessPath
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVolumeMF.DeleteAccessPath
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolumeMF::DeleteAccessPath


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Removes 
   the access path from the current volume.


## -parameters




### -param pwszPath [in]

A string that contains the access path to be removed. An access path can be a drive letter or a path to an empty directory on an NTFS volume. If it is a drive letter, you must include a trailing backslash, for example, "F:\". If it is a path to a directory, the trailing backslash is not required, for example, "C:\MyFolder\MyDocuments".


### -param bForce [in]

If <b>TRUE</b>, the access path is deleted unconditionally, even if the volume is in 
      use. This parameter is meaningful only when the access path is a drive letter.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OPERATION_DENIED</b></dt>
<dt>0x8004240AL</dt>
</dl>
</td>
<td width="60%">
The path leads to the system volume, the boot volume, the crashdump volume, the hibernation volume, or 
       the pagefile volume. You cannot remove the drive letter from these volumes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PATH_NOT_FOUND</b></dt>
<dt>0x80042416L</dt>
</dl>
</td>
<td width="60%">
The specified path is not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DEVICE_IN_USE</b></dt>
<dt>0x80042413L</dt>
</dl>
</td>
<td width="60%">
The access path was deleted successfully, however, an error occurred. VDS possibly failed to update the 
        GUID partition table (GPT) attribute of a partition or failed to delete a default network share (such as F$) 
        while deleting the drive letter.

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



If there are no open handles on the volume, the drive letter is removed immediately. However, if there are open handles on the volume, the volume cannot be locked and the drive letter is removed when the computer is restarted.




## -see-also




<a href="https://msdn.microsoft.com/4c8a63bd-ae2f-4157-92f9-aefc592c7d4f">IVdsVolumeMF</a>



<a href="https://msdn.microsoft.com/cf29639e-33fd-42f6-b616-7145521da347">IVdsVolumeMF::AddAccessPath</a>



<a href="https://msdn.microsoft.com/7d541245-c189-4abe-ac72-2928c7aeed95">IVdsVolumeMF::QueryAccessPaths</a>
 

 

