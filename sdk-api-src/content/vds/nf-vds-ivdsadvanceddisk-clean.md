---
UID: NF:vds.IVdsAdvancedDisk.Clean
title: IVdsAdvancedDisk::Clean (vds.h)
description: Removes partition information and uninitializes basic or dynamic disks.Windows Server 2003:  The Clean method is not supported for removable devices.
helpviewer_keywords: ["Clean","Clean method [VDS]","Clean method [VDS]","IVdsAdvancedDisk interface","IVdsAdvancedDisk interface [VDS]","Clean method","IVdsAdvancedDisk.Clean","IVdsAdvancedDisk::Clean","base.ivdsadvanceddisk_clean","vds/IVdsAdvancedDisk::Clean"]
old-location: base\ivdsadvanceddisk_clean.htm
tech.root: base
ms.assetid: 4052f294-d911-44c6-a57f-0a0a6f24df70
ms.date: 12/05/2018
ms.keywords: Clean, Clean method [VDS], Clean method [VDS],IVdsAdvancedDisk interface, IVdsAdvancedDisk interface [VDS],Clean method, IVdsAdvancedDisk.Clean, IVdsAdvancedDisk::Clean, base.ivdsadvanceddisk_clean, vds/IVdsAdvancedDisk::Clean
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
 - IVdsAdvancedDisk::Clean
 - vds/IVdsAdvancedDisk::Clean
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
 - IVdsAdvancedDisk.Clean
---

# IVdsAdvancedDisk::Clean


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Removes partition information 
   and uninitializes basic or dynamic disks.

<b>Windows Server 2003:  </b>The <b>Clean</b> method is not supported for removable devices.

## -parameters

### -param bForce [in]

If <b>TRUE</b>, cleans a disk containing data volumes or ESP partitions.

### -param bForceOEM [in]

If <b>TRUE</b>, cleans a MBR-based disk containing the known OEM partitions in the following table or cleans a 
      GPT-based disk containing any OEM partition. An OEM partition has the GPT_ATTRIBUTE_PLATFORM_REQUIRED flag set 
      on a GPT-based disk.
      

<table>
<tr>
<th>Partition type</th>
<th>Description</th>
</tr>
<tr>
<td>0x12</td>
<td>An EISA partition.</td>
</tr>
<tr>
<td>0x84</td>
<td>A hibernation partition for laptops.</td>
</tr>
<tr>
<td>0xA0</td>
<td>A diagnostic partition for some HP laptops.</td>
</tr>
<tr>
<td>0xDE</td>
<td>A partition defined by Dell.</td>
</tr>
<tr>
<td>0xFE</td>
<td>An IBM IML partition.</td>
</tr>
</table>

### -param bFullClean [in]

If <b>TRUE</b>, cleans the entire disk by replacing the data on each sector with zeros; otherwise, this method cleans 
      only the first and the last megabytes on the disk.

### -param ppAsync [out]

The address of a pointer to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface 
      pointer, which VDS initializes on return. Callers must release the interface. Use this pointer to cancel, wait 
      for, or query the status of the operation.

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
The data was removed successfully and the disk was uninitialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NO_MEDIA</b></dt>
<dt>0x80042412L</dt>
</dl>
</td>
<td width="60%">
There is no media in the removable device.

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
<dt><b>VDS_E_OPERATION_DENIED</b></dt>
<dt>0x8004240AL</dt>
</dl>
</td>
<td width="60%">
The operation failed under one of the following conditions:
         

<ul>
<li>The disk contains an OEM partition and <i>bForceOEM</i> is false.</li>
<li>The disk contains a volume or ESP partition and <i>bForce</i> is <b>FALSE</b>.</li>
<li>The disk contains one of the system volumes regardless of whether <i>bForce</i> is <b>TRUE</b> 
           or <b>FALSE</b>. A system volume can be any of the following items:
           <ul>
<li>A volume containing the operating system loader.</li>
<li>A boot volume, which contains the system32 directory.</li>
<li>A volume containing the pagefile or hibernation file, or a volume used as a crash dump.</li>
<li>An ESP partition (the partition from which the system boots).</li>
</ul>
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_DISK_PARTIALLY_CLEANED</b></dt>
<dt>0x0004241AL</dt>
</dl>
</td>
<td width="60%">
The partition table is cleaned, but not all sectors are cleaned during a full clean. Alternatively, some 
         sectors of the first megabyte and the last megabyte are cleaned; however, unless the clean is a full clean, 
         the remaining sectors are not cleaned.
        

</td>
</tr>
</table>

## -remarks

Before calling this method, the caller should dismount any mounted volumes on the disk by calling <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-dismount">IVdsVolumeMF::Dismount</a> for each volume.

Use the <i>bForce</i> parameter, the <i>bForceOEM</i> parameter, or both 
    with this method unless you first delete all data volumes, known OEM partitions, and ESP partitions on the disk. 
    This requirement excludes metadata partitions such as the MSR, the LDM metadata partition, and unknown OEM partitions.
   

<b>Windows Server 2003:  </b>The <b>Clean</b> method is not supported for removable devices. 

Implementers must return a pointer to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface for 
      this method, regardless of whether the call initiates an asynchronous operation.

## -see-also

<a href="/windows/desktop/VDS/disk-object">Disk Object</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsadvanceddisk">IVdsAdvancedDisk</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>