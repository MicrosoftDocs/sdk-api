---
UID: NF:vds.IVdsPack.AddDisk
title: IVdsPack::AddDisk (vds.h)
description: Adds a disk to an online pack.
helpviewer_keywords: ["AddDisk","AddDisk method [VDS]","AddDisk method [VDS]","IVdsPack interface","IVdsPack interface [VDS]","AddDisk method","IVdsPack.AddDisk","IVdsPack::AddDisk","base.ivdspack_adddisk","vds/IVdsPack::AddDisk"]
old-location: base\ivdspack_adddisk.htm
tech.root: base
ms.assetid: e64e3891-74c6-4014-9909-24f75f69e06d
ms.date: 12/05/2018
ms.keywords: AddDisk, AddDisk method [VDS], AddDisk method [VDS],IVdsPack interface, IVdsPack interface [VDS],AddDisk method, IVdsPack.AddDisk, IVdsPack::AddDisk, base.ivdspack_adddisk, vds/IVdsPack::AddDisk
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsPack::AddDisk
 - vds/IVdsPack::AddDisk
dev_langs:
 - c++
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
---

# IVdsPack::AddDisk


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Adds a disk to an online pack.

## -parameters

### -param DiskId [in]

The GUID of the disk.

### -param PartitionStyle [in]

The style can be MBR or GPT. See the <a href="/windows/desktop/api/vds/ne-vds-vds_partition_style">VDS_PARTITION_STYLE</a> enumeration.

### -param bAsHotSpare [in]

If true,  VDS can use the disk as a hot spare; otherwise, the disk cannot be used for this operation. Only hardware providers support hot sparing.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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

To undo the effect of this method—that is, to remove the partitioning format and cause the disk to be a raw disk that is owned by the VDS service—use the <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-clean">IVdsAdvancedDisk::Clean</a> method.

You cannot use <b>AddDisk</b> to redefine the partitioning on an existing disk. 



If you add a GPT disk to a basic pack, the	 operation automatically creates a MSR partition on the disk. Devices running the WinPE operating system are the  exception because an administrator might prefer to create an ESP partition on the disk. The ESP partition, if present, must be the first partition on the disk. 

If you add the disk to a dynamic pack, the operation does not create a MSR partition.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdspack">IVdsPack</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_pack_prop">VDS_PACK_PROP</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_partition_style">VDS_PARTITION_STYLE</a>