---
UID: NF:vds.IVdsVolume.Delete
title: IVdsVolume::Delete (vds.h)
description: Deletes the volume and all plexes, releasing the extents.
helpviewer_keywords: ["Delete","Delete method [VDS]","Delete method [VDS]","IVdsVolume interface","IVdsVolume interface [VDS]","Delete method","IVdsVolume.Delete","IVdsVolume::Delete","base.ivdsvolume_delete","vds/IVdsVolume::Delete"]
old-location: base\ivdsvolume_delete.htm
tech.root: base
ms.assetid: 6cc7cb6d-4495-41b7-8fe5-d2e1f574ed70
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [VDS], Delete method [VDS],IVdsVolume interface, IVdsVolume interface [VDS],Delete method, IVdsVolume.Delete, IVdsVolume::Delete, base.ivdsvolume_delete, vds/IVdsVolume::Delete
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
 - IVdsVolume::Delete
 - vds/IVdsVolume::Delete
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
 - IVdsVolume.Delete
---

# IVdsVolume::Delete


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Deletes the volume and all plexes, 
   releasing the extents.

## -parameters

### -param bForce [in]

If <b>TRUE</b>, VDS deletes the volume even if it is  in use; otherwise, the volume is not deleted if it is in use.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The plexes were deleted successfully.

</td>
</tr>
</table>

## -remarks

You can only delete volumes from an online pack. Use the 
    <a href="/windows/desktop/api/vds/nf-vds-ivdspack-getproperties">IVdsPack::GetProperties</a> method to confirm 
    that the pack status is <b>VDS_PS_ONLINE</b>.

You cannot delete a volume that is on removable media.

VDS dismounts the file system before deleting a volume—an operation required by FAT and FAT32, but not NTFS. In 
    addition, VDS deletes all access paths to the volume after deleting the volume itself. If the dismount operation 
    fails, and <i>bForce</i> is <b>true</b>, VDS deletes the volume without a dismount. File system client 
    applications must handle this situation. If the dismount succeeds, and the delete operation fails, VDS attempts 
    to remount the volume.

VDS prevents the deletion of the current system and boot volumes, as well as the pagefile, crashdump, and 
    hibernate volumes. You can move or reset the crashdump and pagefile. The hibernate volume must remain on the boot 
    partition.

<b>Windows Server 2003:  </b>The crashdump and hibernate volumes must remain on the boot partition.

<b>Windows Server 2003:  </b>After the volume has been deleted, VDS tries to delete the mounted folders. If this fails, 
      <b>Delete</b> will return 
      <b>VDS_S_ACCESS_PATH_NOT_DELETED</b>, even though the volume was successfully deleted.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdspack-getproperties">IVdsPack::GetProperties</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_pack_status">VDS_PACK_STATUS</a>