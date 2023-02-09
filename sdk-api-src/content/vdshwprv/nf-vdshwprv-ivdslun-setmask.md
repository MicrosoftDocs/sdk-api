---
UID: NF:vdshwprv.IVdsLun.SetMask
title: IVdsLun::SetMask (vdshwprv.h)
description: The IVdsLun::SetMask (vdshwprv.h) method specifies the unmasking list, which is the list of computers to be granted access to the LUN.
helpviewer_keywords: ["IVdsLun interface [VDS]","SetMask method","IVdsLun.SetMask","IVdsLun::SetMask","SetMask","SetMask method [VDS]","SetMask method [VDS]","IVdsLun interface","base.ivdslun_setmask","vds/IVdsLun::SetMask","vdshwprv/IVdsLun::SetMask"]
old-location: base\ivdslun_setmask.htm
tech.root: base
ms.assetid: b7e841cc-95b4-452f-ac14-d7063fe6a694
ms.date: 08/08/2022
ms.keywords: IVdsLun interface [VDS],SetMask method, IVdsLun.SetMask, IVdsLun::SetMask, SetMask, SetMask method [VDS], SetMask method [VDS],IVdsLun interface, base.ivdslun_setmask, vds/IVdsLun::SetMask, vdshwprv/IVdsLun::SetMask
req.header: vdshwprv.h
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
 - IVdsLun::SetMask
 - vdshwprv/IVdsLun::SetMask
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
 - IVdsLun.SetMask
---

# IVdsLun::SetMask


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Specifies the unmasking list, 
   which is the list of computers to be granted access to the LUN.

## -parameters

### -param pwszUnmaskingList [in]

A list specifying the computers to be granted access to the LUN. The list is a semicolon-delimited, 
       NULL-terminated, human-readable string. 

If the value is "*", all computers that have an HBA 
       port attached to the storage subsystem are to be granted access to the LUN. <div class="alert"><b>Note</b>  In practice, if the value is "*", most hardware providers only grant the ports and initiators on the local computer access to the LUN.</div>
<div> </div>


If the value is 
       "", access is revoked for all computers that were previously granted access to the LUN.

If "*" or "" is specified, no other value can be specified.

For Fibre Channel networks and serial attached SCSI (SAS) networks, each entry is a 64-bit World-Wide Name (WWN) of each port to which the LUN is 
       unmasked, formatted as a hexadecimal string (16 characters long), most significant byte first. For example, a 
       WWN address of 01:23:45:67:89:AB:CD:EF is represented as "0123456789ABCDEF". For more information, see the T10 specifications for <a href="https://t10.org/drafts.htm#FibreChannel">Fibre Channel</a> and <a href="https://t10.org/drafts.htm#SCSI3_SAS">SAS</a>.

For iSCSI networks, each entry is an iSCSI qualified name (IQN) of each initiator to which the LUN is 
       unmasked. A LUN unmasked to a particular initiator is considered to be associated with that initiator.

<div class="alert"><b>Note</b>  The unmasking list can contain the same WWN or IQN more than once. The caller is not expected to remove 
       duplicates from the list or to validate the format of the WWN or iSCSI name. In addition, access is not 
       cumulative. In other words, if this method is called twice in succession, only the computers specified in the 
       second call are granted access.</div>
<div> </div>

## -returns

This method can return standard <b>HRESULT</b> values, such as 
      <b>E_INVALIDARG</b> or <b>E_OUTOFMEMORY</b>, and 
      <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It 
      can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a> using 
      the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate 
      from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is 
      being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
This return value signals a software or communication problem inside a provider that caches information 
        about the array. Use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to restore 
        the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_DELETED</b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The LUN object is no longer present.

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
The LUN is in a failed state, and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress; this operation cannot proceed until the previous operation or 
        operations are complete.

</td>
</tr>
</table>

## -remarks

Before calling the <b>SetMask</b> method to mask a LUN, 
    the caller should uninstall the corresponding disks as follows. First, retrieve the VDS object ID of the disk that 
    corresponds to the LUN being masked by calling 
    <a href="/windows/desktop/api/vds/nf-vds-ivdsserviceuninstalldisk-getdiskidfromluninfo">IVdsServiceUninstallDisk::GetDiskIdFromLunInfo</a>. 
    Then call 
    <a href="/windows/desktop/api/vds/nf-vds-ivdsserviceuninstalldisk-uninstalldisks">IVdsServiceUninstallDisk::UninstallDisks</a> 
    with the VDS object ID of the disk.

<b>Windows Server 2003 and Windows Server 2003 with SP1:  </b>To uninstall the corresponding disks, perform the following steps. Note that these steps became obsolete 
     with Windows Server 2003 R2.
     <ol>
<li>Locate the volumes on the disks to be masked as follows:
       <ol>
<li>For each disk, call the 
         <a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-queryextents">IVdsDisk::QueryExtents</a> method to enumerate 
         the disk extents. This method returns a list of 
         <a href="/windows/desktop/api/vds/ns-vds-vds_disk_extent">VDS_DISK_EXTENT</a> structures. The 
         <b>volumeId</b> member of this structure contains the volume 
         <b>GUID</b>.</li>
<li>Enumerate the volumes managed by the software provider by calling the 
         <a href="/windows/desktop/api/vds/nf-vds-ivdsswprovider-querypacks">IVdsSwProvider::QueryPacks</a> method to 
         enumerate the packs and calling 
         <a href="/windows/desktop/api/vds/nf-vds-ivdspack-queryvolumes">IVdsPack::QueryVolumes</a> to enumerate the 
         volumes in each pack. Call 
         <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-getproperties">IVdsVolume::GetProperties</a> to obtain the 
         <a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop">VDS_VOLUME_PROP</a> structure for each volume. The 
         <b>id</b> member of this structure contains the volume <b>GUID</b>. 
         The <b>pwszName</b> member contains the volume name to be passed to 
         <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> to obtain a volume handle.</li>
<li>Use the volume GUIDs that were obtained by calling 
         <a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-queryextents">IVdsDisk::QueryExtents</a> to determine which of 
         the volume names you will need from the list of enumerated volumes.</li>
</ol>
</li>
<li>Lock each volume by using the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lock_volume">FSCTL_LOCK_VOLUME</a> 
       control code. If the LUN is being moved to another machine as an intact volume, and another application holds a 
       volume lock, you should retry the <b>FSCTL_LOCK_VOLUME</b> 
       operation if possible before continuing on to the next step. However, if the volume is only being locked and 
       dismounted because it is being deleted, there is no need to retry the 
       <b>FSCTL_LOCK_VOLUME</b> operation.
       <div class="alert"><b>Note</b>  This step is optional. The purpose of this step is to allow other applications that may hold locks to 
        release them. Even if the lock operation fails, you should continue on to the next step.</div>
<div> </div>
</li>
<li>Dismount each volume by using the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_unlock_volume">FSCTL_DISMOUNT_VOLUME</a> control code.</li>
<li>If the volumes are on basic disks, take them offline by using the 
       <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_volume_offline">IOCTL_VOLUME_OFFLINE</a> control code.</li>
<li>Uninstall each volume using the <b>SetupDiCallClassInstaller</b> function, 
       passing <b>DIF_REMOVE</b> for the <i>InstallFunction</i> parameter.</li>
<li>Uninstall each disk using the <b>SetupDiCallClassInstaller</b> function, passing 
       <b>DIF_REMOVE</b> for the <i>InstallFunction</i> parameter.</li>
<li>Remove user-mode paths, such as mounted folders and drive-letter assignments, from the registry by calling 
       the 
       <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-cleanupobsoletemountpoints">IVdsService::CleanupObsoleteMountPoints</a> 
       method.</li>
</ol>


After a LUN is unmasked to a target machine or masked from a target machine, the LUN's visibility on that 
    machine may not change until a bus rescan is performed. The VDS application on the target machine initiates the 
    bus rescan by calling <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-reenumerate">IVdsService::Reenumerate</a>. 
    The initiating of the bus rescan is the responsibility of the VDS application, not the hardware provider.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>
