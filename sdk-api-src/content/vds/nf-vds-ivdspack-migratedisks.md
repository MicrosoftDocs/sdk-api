---
UID: NF:vds.IVdsPack.MigrateDisks
title: IVdsPack::MigrateDisks (vds.h)
description: Migrates a set of disks from one pack to another pack.
helpviewer_keywords: ["IVdsPack interface [VDS]","MigrateDisks method","IVdsPack.MigrateDisks","IVdsPack::MigrateDisks","MigrateDisks","MigrateDisks method [VDS]","MigrateDisks method [VDS]","IVdsPack interface","base.ivdspack_migratedisks","vds/IVdsPack::MigrateDisks"]
old-location: base\ivdspack_migratedisks.htm
tech.root: base
ms.assetid: c7e85c4c-fb7c-48de-abd7-8d65ecb9a1fa
ms.date: 12/05/2018
ms.keywords: IVdsPack interface [VDS],MigrateDisks method, IVdsPack.MigrateDisks, IVdsPack::MigrateDisks, MigrateDisks, MigrateDisks method [VDS], MigrateDisks method [VDS],IVdsPack interface, base.ivdspack_migratedisks, vds/IVdsPack::MigrateDisks
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
 - IVdsPack::MigrateDisks
 - vds/IVdsPack::MigrateDisks
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
 - IVdsPack.MigrateDisks
---

# IVdsPack::MigrateDisks


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Migrates a set of disks 
   from one pack to another pack.

## -parameters

### -param pDiskArray [in]

A pointer to an array of GUIDs; one for each disk.

### -param lNumberOfDisks [in]

The number of disks to migrate.

### -param TargetPack [in]

The GUID of the pack object.

### -param bForce [in]

If this parameter is set to <b>TRUE</b>, VDS ignores all errors from this method and attempts to migrate the disks unconditionally. If it is set to <b>FALSE</b>, the 
      operation does not proceed. In some cases, a forced migration can cause data loss.

### -param bQueryOnly [in]

If this parameter is set to <b>TRUE</b>, the migration does not occur. If it is set to <b>FALSE</b>, the operation proceeds.

### -param pResults [out]

The address of a caller-allocated array of <b>HRESULT</b> values.
       The number of elements in the array is <i>lNumberOfDisks</i>.

If a disk can be migrated, or was migrated successfully, the corresponding array element receives 
      <b>S_OK</b>; otherwise, it receives the warning code or error code that was returned by the provider. For the list 
      of additional result codes, see Return Values.

### -param pbRebootNeeded [out]

If this parameter is set to <b>TRUE</b>, you must restart the computer to complete the operation. If it is set to <b>FALSE</b>, the operation completes without restarting.

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
The migration completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
At least one of the disks cannot be converted, or can be converted with warning.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DISK_NOT_ONLINE</b></dt>
<dt>0x8004244BL</dt>
</dl>
</td>
<td width="60%">
One of the disks is unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_IMPORT_SET_INCOMPLETE</b></dt>
<dt>0x80042451L</dt>
</dl>
</td>
<td width="60%">
An attempt was made to import a subset of the disks in the foreign pack.

</td>
</tr>
</table>
 

The following warnings and errors can be returned through <i>pResults</i>:

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_BOOT_PARTITION_NUMBER_CHANGE</b></dt>
<dt>0x00042436L</dt>
</dl>
</td>
<td width="60%">
The partition number of the boot partition changed as the result of the migration operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NO_FREE_SPACE</b></dt>
<dt>0x80042437L</dt>
</dl>
</td>
<td width="60%">
The selected disk does not have enough free space to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ACTIVE_PARTITION</b></dt>
<dt>0x80042438L</dt>
</dl>
</td>
<td width="60%">
An active partition was detected on the selected disk, and it is not the active partition used to boot the 
        active operating system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PARTITION_OF_UNKNOWN_TYPE</b></dt>
<dt>0x80042439L</dt>
</dl>
</td>
<td width="60%">
The partition information cannot be read.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_LEGACY_VOLUME_FORMAT</b></dt>
<dt>0x8004243AL</dt>
</dl>
</td>
<td width="60%">
A partition with an unknown type was detected on the selected disk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NON_CONTIGUOUS_DATA_PARTITIONS</b></dt>
<dt>0x8004243BL</dt>
</dl>
</td>
<td width="60%">
The selected GPT disk contains a non-basic data partition, which is both preceded by and followed by one 
        or more basic data partitions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_MIGRATE_OPEN_VOLUME</b></dt>
<dt>0x8004243CL</dt>
</dl>
</td>
<td width="60%">
A volume on the selected disk cannot be opened.

</td>
</tr>
</table>

## -remarks

VDS implements this method.

A single pack can have only one basic disk. As such, you can migrate only one disk at a time between a basic and dynamic pack.

You should force this operation when converting a basic disk to dynamic disk format and the end of the disk lacks 
    enough space for the LDM database. Set the <i>bForce</i> parameter to <b>true</b> and force the 
    operation despite the space limitation. Likewise, if an OEM partition is in the middle of a MBR disk with free 
    space or data volumes on either side.

After migrating dynamic disks to a dynamic pack, you should use the <a href="/windows/desktop/api/vds/nf-vds-ivdspack-getproperties">IVdsPack::GetProperties</a> method to determine whether the source or destination pack is now the online pack.

For information about using the <b>MigrateDisks</b> method to add foreign disks to a pack, see <a href="/windows/desktop/VDS/adding-foreign-disks-to-a-pack">Adding Foreign Disks to a Pack</a>.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdspack">IVdsPack</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdspack-getproperties">IVdsPack::GetProperties</a>