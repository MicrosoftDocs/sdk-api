---
UID: NF:vds.IVdsDiskPartitionMF.GetPartitionFileSystemProperties
title: IVdsDiskPartitionMF::GetPartitionFileSystemProperties
author: windows-sdk-content
description: Returns property details about the file system on a partition on the disk at a specified byte offset.
old-location: base\ivdsdiskpartitionmf_getpartitionfilesystemproperties.htm
old-project: vds
ms.assetid: 1b49ffba-00df-4d8f-a90f-5e26a5c898dd
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: GetPartitionFileSystemProperties, GetPartitionFileSystemProperties method, GetPartitionFileSystemProperties method,IVdsDiskPartitionMF interface, IVdsDiskPartitionMF interface,GetPartitionFileSystemProperties method, IVdsDiskPartitionMF.GetPartitionFileSystemProperties, IVdsDiskPartitionMF::GetPartitionFileSystemProperties, base.ivdsdiskpartitionmf_getpartitionfilesystemproperties, vds/IVdsDiskPartitionMF::GetPartitionFileSystemProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVdsDiskPartitionMF.GetPartitionFileSystemProperties
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsDiskPartitionMF::GetPartitionFileSystemProperties


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns property details about the file system on a partition on the disk at a specified byte offset.


## -parameters




### -param ullOffset [in]

Byte offset of the partition from the beginning of the disk.  This offset must be the offset of the start of a partition.


### -param pFileSystemProp [out]

Pointer to a <a href="https://msdn.microsoft.com/1068eb6d-0f7f-4d04-b7ec-f40e54ff8325">VDS_FILE_SYSTEM_PROP</a> structure that upon successful completion receives the properties of the file system volume on the partition.


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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_BAD_PROVIDER_DATA</b></dt>
<dt>0x80042441L</dt>
</dl>
</td>
<td width="60%">
A provider returned bad data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DISK_REMOVEABLE</b></dt>
<dt>0x8004255AL</dt>
</dl>
</td>
<td width="60%">
The operation is not supported on removable media.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_MISSING_DISK</b></dt>
<dt>0x80042454L</dt>
</dl>
</td>
<td width="60%">
The disk is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
The partition does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PARTITION_NOT_OEM</b></dt>
<dt>0x8004256FL</dt>
</dl>
</td>
<td width="60%">
The operation is not supported on non-OEM partitions.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/84d0918d-479f-4026-b120-11cc21a43233">IVdsDiskPartitionMF</a>
 

 

