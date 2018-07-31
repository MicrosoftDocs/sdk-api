---
UID: NF:vds.IVdsServiceUninstallDisk.UninstallDisks
title: IVdsServiceUninstallDisk::UninstallDisks
author: windows-sdk-content
description: Uninstalls a set of disks.
old-location: base\ivdsserviceuninstalldisk_uninstalldisks.htm
old-project: VDS
ms.assetid: 65c5444f-7e97-4746-9d74-561dc435212d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVdsServiceUninstallDisk interface,UninstallDisks method, IVdsServiceUninstallDisk.UninstallDisks, IVdsServiceUninstallDisk::UninstallDisks, UninstallDisks, UninstallDisks method, UninstallDisks method,IVdsServiceUninstallDisk interface, base.ivdsserviceuninstalldisk_uninstalldisks, vds/IVdsServiceUninstallDisk::UninstallDisks
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVdsServiceUninstallDisk.UninstallDisks
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsServiceUninstallDisk::UninstallDisks


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Uninstalls a set of disks.


## -parameters




### -param pDiskIdArray [in]

Address of a buffer containing an array of VDS object IDs, one for each disk to be uninstalled. Each ID in 
      the array must be unique.


### -param ulCount [in]

Number of VDS object IDs in the buffer that the <i>pDiskIdArray</i> parameter points 
      to.


### -param bForce [in]

If <b>TRUE</b>, VDS uninstalls the disks even if the volumes cannot be locked or 
      dismounted.


### -param pbReboot [out]

Address of a <b>BOOLEAN</b> variable that receives <b>TRUE</b> if 
      the user must restart the computer to complete the uninstall process.


### -param pResults [out]

The address of a caller-allocated array of <b>HRESULT</b> values. The number of elements in the array is pointed to by the 
      <i>pDiskIdArray</i> parameter. The first element of this array corresponds to the 
      first element in the <i>pDiskIdArray</i>, and so on. If any of the disks fails to initialize 
      properly, the specific error code for the failure is returned in the corresponding element of this array.


## -returns



This method can return standard <b>HRESULT</b> values, such as 
      <b>E_INVALIDARG</b> or <b>E_OUTOFMEMORY</b>, and 
      <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It 
      can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a> using 
      the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate 
      from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is 
      being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The disks were successfully uninstalled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
This method returned a warning or error code for one or more disks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_UNABLE_TO_GET_GPT_ATTRIBUTES</b></dt>
<dt>0x0004245BL</dt>
</dl>
</td>
<td width="60%">
The disks were successfully uninstalled, but the GUID partition table (GPT) attributes could not be 
        retrieved for one or more disks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INTERNAL_ERROR</b></dt>
<dt>0x80042448L</dt>
</dl>
</td>
<td width="60%">
VDS encountered an internal error. Check the event log for more information.

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
One or more disks were missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NO_DISK_PATHNAME</b></dt>
<dt>0x8004270FL</dt>
</dl>
</td>
<td width="60%">
The path could not be retrieved for one or more disks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NO_VOLUME_PATHNAME</b></dt>
<dt>0x80042711L</dt>
</dl>
</td>
<td width="60%">
The path could not be retrieved for one or more volumes.

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
One or more of the specified VDS object IDs correspond to disks that are no longer present.

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
One or more of the specified VDS object IDs correspond to disks that do not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_OUTOFSYNC</b></dt>
<dt>0x80042712L</dt>
</dl>
</td>
<td width="60%">
The provider's cache is not in sync with the driver cache.

</td>
</tr>
</table>
 




## -remarks



VDS implements this method.

This method, which is synchronous, first uninstalls the volumes on the specified disks, and then uninstalls the 
    disks. After the disks are uninstalled, the corresponding LUNs can be masked (hidden) or deleted.

This method cleans up the drive letters that were assigned to the volumes on the disks. In addition, it sets 
    the volumes offline to prevent a volume from being remounted after the dismount handle has been closed but before 
    the disk is actually removed.

When removing a dynamic volume that spans more than one disk, you must call this method instead of using device manager functions.

For instructions on how to uninstall a disk on Windows Server 2003 releases where the 
    <b>UninstallDisks</b> 
    method is not supported, see the Remarks section of the <a href="https://msdn.microsoft.com/b7e841cc-95b4-452f-ac14-d7063fe6a694">IVdsLun::SetMask</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/2d111105-9970-40a3-bb8d-a92d38985fd9">IVdsServiceUninstallDisk</a>
 

 

