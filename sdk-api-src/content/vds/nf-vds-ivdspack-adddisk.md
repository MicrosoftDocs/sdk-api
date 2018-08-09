---
UID: NF:vds.IVdsPack.AddDisk
title: IVdsPack::AddDisk
author: windows-sdk-content
description: Adds a disk to an online pack.
old-location: base\ivdspack_adddisk.htm
old-project: vds
ms.assetid: e64e3891-74c6-4014-9909-24f75f69e06d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: AddDisk, AddDisk method [VDS], AddDisk method [VDS],IVdsPack interface, IVdsPack interface [VDS],AddDisk method, IVdsPack.AddDisk, IVdsPack::AddDisk, base.ivdspack_adddisk, vds/IVdsPack::AddDisk
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
 - IVdsPack.AddDisk
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsPack::AddDisk


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Adds a disk to an online pack.


## -parameters




### -param DiskId [in]

The GUID of the disk.


### -param PartitionStyle [in]

The style can be MBR or GPT. See the <a href="https://msdn.microsoft.com/31b7f0b3-cc3c-48e7-a4f0-628f0185f3cb">VDS_PARTITION_STYLE</a>enumeration.


### -param bAsHotSpare [in]

If true,  VDS can use the disk as a hot spare; otherwise, the disk cannot be used for this operation. Only hardware providers support hot sparing.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The disk was added successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_AN_UNALLOCATED_DISK</b></dt>
<dt>0x80042418L</dt>
</dl>
</td>
<td width="60%">
The disk is raw.

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
The disk to be added is being cleaned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_FAILURE</b></dt>
<dt>0x80042442L</dt>
</dl>
</td>
<td width="60%">
There is a provider failure during the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
Adding a second disk to a basic pack is not supported.

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
The target pack is inaccessible.

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
The disk is not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DMADMIN_METHOD_CALL_FAILED</b></dt>
<dt>0x80042420L</dt>
</dl>
</td>
<td width="60%">
The logical disk manager (LDM) service failed to complete a method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The dynamic provider cache is corrupt.

</td>
</tr>
</table>
 




## -remarks



VDS implements this method.

This method initializes a raw disk (a disk that has no partitioning defined) and adds it to the pack. Before this method is called, the raw disk is owned by the VDS service. After this method returns, the disk is owned by the basic provider.

To undo the effect of this method—that is, to remove the partitioning format and cause the disk to be a raw disk that is owned by the VDS service—use the <a href="https://msdn.microsoft.com/4052f294-d911-44c6-a57f-0a0a6f24df70">IVdsAdvancedDisk::Clean</a> method.

You cannot use <b>AddDisk</b> to redefine the partitioning on an existing disk. 



If you add a GPT disk to a basic pack, the	 operation automatically creates a MSR partition on the disk. Devices running the WinPE operating system are the  exception because an administrator might prefer to create an ESP partition on the disk. The ESP partition, if present, must be the first partition on the disk. 

If you add the disk to a dynamic pack, the operation does not create a MSR partition.






## -see-also




<a href="https://msdn.microsoft.com/106989fe-d1dd-4c7f-b889-00a671c6e567">IVdsPack</a>



<a href="https://msdn.microsoft.com/5d04bf6c-fda2-4b95-a8bb-907e64267f30">VDS_PACK_PROP</a>



<a href="https://msdn.microsoft.com/31b7f0b3-cc3c-48e7-a4f0-628f0185f3cb">VDS_PARTITION_STYLE</a>
 

 

