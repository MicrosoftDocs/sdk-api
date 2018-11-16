---
UID: NF:vds.IVdsPack2.CreateVolume2
title: IVdsPack2::CreateVolume2
author: windows-sdk-content
description: Creates a volume in a disk pack with an optional alignment parameter.
old-location: base\ivdspack2_createvolume2.htm
tech.root: VDS
ms.assetid: cc7de88b-af6c-4d39-9297-49e33810466a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateVolume2, CreateVolume2 method, CreateVolume2 method,IVdsPack2 interface, IVdsPack2 interface,CreateVolume2 method, IVdsPack2.CreateVolume2, IVdsPack2::CreateVolume2, base.ivdspack2_createvolume2, vds/IVdsPack2::CreateVolume2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsPack2.CreateVolume2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vds.h
: 
- IVdsPack2.CreateVolume2
: 
---

# IVdsPack2::CreateVolume2


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Creates a volume in a disk pack with an optional alignment parameter.


## -parameters




### -param type [in]

Value from the <a href="https://msdn.microsoft.com/07a44bbf-0726-4094-9b5f-2d26b0030796">VDS_VOLUME_TYPE</a> enumeration that indicates the type of volume to create.


### -param pInputDiskArray [in]

Array of <a href="https://msdn.microsoft.com/837981e5-8600-4add-85cf-a802615133d3">VDS_INPUT_DISK</a> structures that indicate the disks on which to create the volume.

<div class="alert"><b>Note</b>  This array's size must be 32 objects or less, because Windows imposes a limit where no more than 32 disks may be used with a single volume.</div>
<div> </div>

### -param lNumberOfDisks [in]

Number of elements in the array pointed to by the <i>pInputDiskArray</i> parameter.


### -param ulStripeSize [in]

Stripe size, in bytes, of the new volume.

<div class="alert"><b>Note</b>  The stripe size must be 65536 if the type is VDS_VT_STRIPE or VDS_VT_PARITY; otherwise, the stripe size MUST be 0.</div>
<div> </div>

### -param ulAlign [in]

Number of bytes for volume alignment.  This parameter is optional and can be zero. If zero is specified, the server will determine the alignment value depending on the size of the disk on which the volume is created.

<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>On a basic disk, the <b>CreateVolume2</b> method ignores  this parameter and the <b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\vds\Alignment</b> registry key. This is a known issue and is being addressed. As a workaround, use the <a href="https://msdn.microsoft.com/94f80a9f-459f-4f3d-8d85-e5ec7d5734c4">IVdsAdvancedDisk::CreatePartition</a>  or <a href="https://msdn.microsoft.com/c9ab5a24-b0b3-41cc-a4bf-3619f156008c">IVdsCreatePartitionEx::CreatePartitionEx</a> method to create partitions on the basic disk so that they are aligned correctly.Dynamic partitions and volumes are aligned using the values under the following registry key:

<b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\vds\Alignment</b>

The default alignment is 1 MB if the disk is 4 GB or larger, or 64 KB if the disk is smaller than 4 GB.




### -param ppAsync [out]

Pointer to an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface that upon successful completion receives the <b>IVdsAsync</b> interface to monitor and control this operation.  Callers must release the interface received when they are done with it.  If the <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> method is called on the interface and a success HRESULT value is returned, the interfaces returned in the <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure must be released by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="https://msdn.microsoft.com/en-us/library/ms687197(v=VS.85).aspx">SUCCEEDED</a> and <a href="https://msdn.microsoft.com/en-us/library/ms693474(v=VS.85).aspx">FAILED</a> macros defined in Winerror.h.


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
The volume was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_NO_NOTIFICATION</b></dt>
<dt>0x00042517L</dt>
</dl>
</td>
<td width="60%">
No volume arrival notification was received. You may need to call <a href="https://msdn.microsoft.com/ca6a1143-b5f0-49e5-8505-836c565aabcf">IVdsService::Refresh</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_UPDATE_BOOTFILE_FAILED</b></dt>
<dt>0x00042434L</dt>
</dl>
</td>
<td width="60%">
The volume is created successfully, but VDS failed to update the boot options in the Boot Configuration Data (BCD) store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ALIGN_IS_ZERO</b></dt>
<dt>0x80042590L</dt>
</dl>
</td>
<td width="60%">
The specified alignment is zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ALIGN_NOT_A_POWER_OF_TWO</b></dt>
<dt>0x8004258FL</dt>
</dl>
</td>
<td width="60%">
The specified alignment is not a power of two.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DISK_NOT_FOUND_IN_PACK</b></dt>
<dt>0x8004252DL</dt>
</dl>
</td>
<td width="60%">
The specified disks do not belong to the same pack.

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
The LDM service failed a method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_EXTENT_SIZE_LESS_THAN_MIN</b></dt>
<dt>0x80042433L</dt>
</dl>
</td>
<td width="60%">
The extent size passed in is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_DISK_COUNT</b></dt>
<dt>0x80042526L</dt>
</dl>
</td>
<td width="60%">
The number of disks specified is not valid for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_MEMBER_COUNT</b></dt>
<dt>0x80042522L</dt>
</dl>
</td>
<td width="60%">
The member count for the volume must be greater than zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_MEMBER_ORDER</b></dt>
<dt>0x80042524L</dt>
</dl>
</td>
<td width="60%">
The member indexes must be monotonically increasing and begin with zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_OPERATION</b></dt>
<dt>0x80042415L</dt>
</dl>
</td>
<td width="60%">
The disk passed in is a CD-ROM or DVD device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_PACK</b></dt>
<dt>0x8004251AL</dt>
</dl>
</td>
<td width="60%">
This operation is not allowed on this disk pack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_PLEX_COUNT</b></dt>
<dt>0x80042521L</dt>
</dl>
</td>
<td width="60%">
The plex count for the volume must be greater than zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_PLEX_ORDER</b></dt>
<dt>0x80042523L</dt>
</dl>
</td>
<td width="60%">
The plex indexes must be monotonically increasing and begin with zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_STRIPE_SIZE</b></dt>
<dt>0x80042525L</dt>
</dl>
</td>
<td width="60%">
The stripe size in bytes must be a power of 2 for striped and RAID-5 volume types and must be zero for all other volume types.

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
The specified disk is missing.

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
There is no media in a removable drive passed in through the disk array.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_ENOUGH_SPACE</b></dt>
<dt>0x8004240FL</dt>
</dl>
</td>
<td width="60%">
There is not enough space on one of the disks.

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
The volume type is not supported.

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
At least one of the disks passed in is not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ONE_EXTENT_PER_DISK</b></dt>
<dt>0x80042531L</dt>
</dl>
</td>
<td width="60%">
A single disk cannot contribute to multiple members or multiple plexes of the same volume.

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
<dt><b>VDS_E_PARTITION_LIMIT_REACHED</b></dt>
<dt>0x80042407L</dt>
</dl>
</td>
<td width="60%">
The maximum number of partitions (primary partitions or primary partitions with an extended partition) 
        already exists when the caller tries to create an additional primary partition or extended partition.

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
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_DISK_COUNT_MAX_EXCEEDED</b></dt>
<dt>0x80042529L</dt>
</dl>
</td>
<td width="60%">
No more than 32 disks are allowed per volume.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_TOO_SMALL</b></dt>
<dt>0x8004242CL</dt>
</dl>
</td>
<td width="60%">
The volume size is too small.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b0124293-693d-412a-a97f-d0dae05a3bfc">IVdsPack2</a>



<a href="https://msdn.microsoft.com/26fea1a4-f060-49e2-a7ac-0e751f798c72">IVdsPack::CreateVolume</a>
 

 

