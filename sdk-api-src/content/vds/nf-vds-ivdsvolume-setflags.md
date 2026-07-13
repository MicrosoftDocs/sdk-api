---
UID: NF:vds.IVdsVolume.SetFlags
title: IVdsVolume::SetFlags (vds.h)
description: Sets the volume flags.
helpviewer_keywords: ["IVdsVolume interface [VDS]","SetFlags method","IVdsVolume.SetFlags","IVdsVolume::SetFlags","SetFlags","SetFlags method [VDS]","SetFlags method [VDS]","IVdsVolume interface","base.ivdsvolume_setflags","vds/IVdsVolume::SetFlags"]
old-location: base\ivdsvolume_setflags.htm
tech.root: base
ms.assetid: f426b089-6c5f-4ab4-aa92-127e24cb57b1
ms.date: 12/05/2018
ms.keywords: IVdsVolume interface [VDS],SetFlags method, IVdsVolume.SetFlags, IVdsVolume::SetFlags, SetFlags, SetFlags method [VDS], SetFlags method [VDS],IVdsVolume interface, base.ivdsvolume_setflags, vds/IVdsVolume::SetFlags
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
 - IVdsVolume::SetFlags
 - vds/IVdsVolume::SetFlags
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
 - IVdsVolume.SetFlags
---

# IVdsVolume::SetFlags


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the volume 
   flags.

## -parameters

### -param ulFlags [in]

The flags enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_volume_flag">VDS_VOLUME_FLAG</a>. Callers 
      can set the following flags: 

* `VDS_VF_LBN_REMAP_ENABLED`
* `VDS_VF_HIDDEN`
* `VDS_VF_READONLY`
* `VDS_VF_NO_DEFAULT_DRIVE_LETTER`
* `VDS_VF_INSTALLABLE`
* `VDS_VF_SHADOW_COPY`

### -param bRevertOnClose [in]

If <b>TRUE</b>, the flags are temporarily set. VDS resets each 
      flag to the previous state when the caller releases the last reference to the volume object, calls 
      <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-clearflags">IVdsVolume::ClearFlags</a>, or dismounts the volume, 
      except when the flag is set on the entire disk (see the table in the Remarks section for details). When the flag 
      is set on the entire disk, the 
      <b>IVdsVolume::ClearFlags</b> method must be called to 
      reset the flags.

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
The flags are set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_LBN_REMAP_ENABLED_FLAG</b></dt>
<dt>0x80042456L</dt>
</dl>
</td>
<td width="60%">
The provider does not support the <b>VDS_VF_LBN REMAP_ENABLED</b> volume 
        flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NO_DRIVELETTER_FLAG</b></dt>
<dt>0x80042457L</dt>
</dl>
</td>
<td width="60%">
The provider does not support the <b>VDS_VF_NO DRIVELETTER</b> volume flag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_REVERT_ON_CLOSE</b></dt>
<dt>0x80042458L</dt>
</dl>
</td>
<td width="60%">
<i>bRevertOnClose</i> should only be set to true if either the 
        <b>VDS_VF_HIDDEN</b> or <b>VDS_VF_READONLY</b> volume flag is 
        set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_REVERT_ON_CLOSE_SET</b></dt>
<dt>0x80042459L</dt>
</dl>
</td>
<td width="60%">
Some volume flags are set to true already. You must clear these flags first, then call this method and 
        set the <i>bRevertOnClose</i> parameter to true again. The 
        <b>VDS_E_INVALID_OPERATION</b> return value can also indicate this condition.

</td>
</tr>
</table>

## -remarks

The <b>VDS_VF_READONLY</b>, <b>VDS_VF_HIDDEN</b>, and 
    <b>VDS_VF_NO_DEFAULT_DRIVE_LETTER</b> flags scope differently depending on the disk type (basic 
    or dynamic) and partition style (MBR or GPT). The scope is either disk-based or volume-based, as described by the 
    following conditions: 

<ul>
<li>If the disk is basic and MBR, then setting one of these flags on a volume affects the current volume and 
      all future volumes with the specified attribute created on the disk.</li>
<li>If the disk is basic and GPT, dynamic and MBR, or dynamic and GPT, then setting one of the flags on a 
      volume applies to that specific volume only.</li>
</ul>
The following table identifies the scope of each volume flag on MBR basic disks, GPT basic disks, and MBR or 
    GPT dynamic disks.

<table>
<tr>
<th>Flag</th>
<th>MBR basic disks</th>
<th>GPT basic disks</th>
<th>MBR or GPT dynamic disks</th>
</tr>
<tr>
<td><b>VDS_VF_LBN_REMAP_ENABLED</b></td>
<td>Cannot be set.</td>
<td>Cannot be set.</td>
<td>Set on volume, if supported by third party volume manager.</td>
</tr>
<tr>
<td><b>VDS_VF_HIDDEN</b></td>
<td>Set on the entire disk.</td>
<td>Set on volumes (data partitions only).</td>
<td>Set on volumes.</td>
</tr>
<tr>
<td><b>VDS_VF_READONLY</b></td>
<td>Set on the entire disk.</td>
<td>Set on volumes (data partitions only).</td>
<td>Set on volumes.</td>
</tr>
<tr>
<td><b>VDS_VF_NO_DEFAULT_DRIVE_LETTER</b></td>
<td>Set on the entire disk.</td>
<td>Set on partitions.</td>
<td>See <a href="/windows/desktop/api/vds/ne-vds-vds_volume_flag">VDS_VOLUME_FLAG</a>.</td>
</tr>
<tr>
<td><b>VDS_VF_SHADOW_COPY</b></td>
<td>Set on the entire disk.</td>
<td>Set on volumes (data partitions only).</td>
<td>Set on volumes.</td>
</tr>
<tr>
<td><b>VDS_VF_INSTALLABLE</b></td>
<td>Cannot be set.</td>
<td>Cannot be set.</td>
<td>Set on volumes.</td>
</tr>
</table>
 

If <i>bRevertOnClose</i> is <b>TRUE</b> and the disk is an MBR basic 
     disk and the volume is then deleted, the flags are still set on the entire disk and the flags will apply to any new volumes 
     that are created on the disk. <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-clean">IVdsAdvancedDisk::Clean</a> 
     must then be used to clear the flags.

To create a boot volume on a dynamic disk, you must set the <b>VDS_VF_INSTALLABLE</b> flag for the volume and then format the volume by calling the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-format">IVdsVolumeMF::Format</a> method.

This method fails if the volume contains one or more of the following flags: 
     <ul>
<li><b>VDS_VF_SYSTEM</b></li>
<li><b>VDS_VF_BOOT</b></li>
<li><b>VDS_VF_PAGEFILE</b></li>
<li><b>VDS_VF_HIBERNATION</b></li>
<li><b>VDS_VF_CRASHDUMP</b></li>
</ul>


Specifying either <b>VDS_VF_HIDDEN</b> or <b>VDS_VF_READONLY</b> will 
     force a dismount and remount of the volume, unless <i>bRevertOnClose</i> is 
     <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-clean">IVdsAdvancedDisk::Clean</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-clearflags">IVdsVolume::ClearFlags</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_volume_flag">VDS_VOLUME_FLAG</a>