---
UID: NF:vds.IVdsVolumeShrink.Shrink
title: IVdsVolumeShrink::Shrink (vds.h)
description: Shrinks the volume and all plexes and returns the released extents.
helpviewer_keywords: ["IVdsVolumeShrink interface","Shrink method","IVdsVolumeShrink.Shrink","IVdsVolumeShrink::Shrink","Shrink","Shrink method","Shrink method","IVdsVolumeShrink interface","base.ivdsvolumeshrink_shrink","vds/IVdsVolumeShrink::Shrink"]
old-location: base\ivdsvolumeshrink_shrink.htm
tech.root: base
ms.assetid: a6d91cb0-b9a4-4a5f-94bc-824b1691bcd7
ms.date: 12/05/2018
ms.keywords: IVdsVolumeShrink interface,Shrink method, IVdsVolumeShrink.Shrink, IVdsVolumeShrink::Shrink, Shrink, Shrink method, Shrink method,IVdsVolumeShrink interface, base.ivdsvolumeshrink_shrink, vds/IVdsVolumeShrink::Shrink
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsVolumeShrink::Shrink
 - vds/IVdsVolumeShrink::Shrink
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
 - IVdsVolumeShrink.Shrink
---

# IVdsVolumeShrink::Shrink


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Shrinks the volume and all plexes and returns the released extents.

## -parameters

### -param ullDesiredNumberOfReclaimableBytes [in]

Maximum number of bytes by which to shrink the size of the volume. The value of this parameter must be greater than or equal to the value of the <i>ullMinNumberOfReclaimableBytes</i> parameter.  If the number of bytes specified is not a multiple of the file system cluster size, the <b>Shrink</b> method will round this value up to the next multiple of the file system cluster size.

### -param ullMinNumberOfReclaimableBytes [in]

Minimum number of bytes by which to shrink the size of the volume.  If the volume size cannot be shrunk by at least this number of bytes, the <b>Shrink</b> method fails.  If the number of bytes specified is not a multiple of the file system cluster size, the <b>Shrink</b> method will round this value up to the next multiple of the file system cluster size.  Specify zero to indicate that no minimum number of reclaimable bytes is required for the <b>Shrink</b> method to succeed.

### -param ppAsync [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer. VDS 
      initializes the interface on return. Callers must release the interface. Use this interface to cancel, wait for, 
      or query the status of the operation. If 
      <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> is called and a success HRESULT value is returned, the interfaces returned in 
      the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure must be released by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros defined in Winerror.h.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CANNOT_SHRINK</b></dt>
<dt>0x8004251EL</dt>
</dl>
</td>
<td width="60%">
The volume cannot be shrunk because the file system does not support it.

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
<dt><b>VDS_E_INTERNAL_ERROR</b></dt>
<dt>0x80042448L</dt>
</dl>
</td>
<td width="60%">
An internal error occurred. Check the event log for more details.

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
No volume arrival notification was received. You may need to call <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-refresh">IVdsService::Refresh</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_SHRINK_SIZE_TOO_BIG</b></dt>
<dt>0x80042574L</dt>
</dl>
</td>
<td width="60%">
The specified shrink size is too large and will cause the volume to be smaller than the minimum volume size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_SHRINK_SIZE_LESS_THAN_MIN</b></dt>
<dt>0x80042573L</dt>
</dl>
</td>
<td width="60%">
The specified shrink size is less than the minimum shrink size allowed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_NOT_HEALTHY</b></dt>
<dt>0x8004243EL</dt>
</dl>
</td>
<td width="60%">
The volume is not healthy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_SIMPLE_SPANNED</b></dt>
<dt>0x80042589L</dt>
</dl>
</td>
<td width="60%">
The operation is only supported on simple or spanned volumes.

</td>
</tr>
</table>

## -remarks

The <b>Shrink</b> method moves the files so that they are as close as possible to the beginning of the volume, in order to consolidate free space at the end of the volume.  (The amount of free space that can be consolidated at the end of the volume determines how much the volume can be shrunk.) It then truncates the file system volume, reducing its size, and then truncates the partition or dynamic volume.

In almost all cases, there will be some files that are immovable (that is, files that cannot be moved). For example, file system and storage driver metadata files are likely to be immovable. For this reason, the amount by which a volume can be shrunk is usually less than the total amount of free space on the volume.

The number and placement of immovable files can vary from one computer to the next, even if both computers are configured identically.

It is possible for a file to be temporarily immovable. For this reason, an application may be able to recover additional space if it calls this method a second time with the same parameters.

If the <i>ullDesiredNumberOfReclaimableBytes</i> and <i>ullMinNumberOfReclaimableBytes</i> parameters are both zero, the <b>Shrink</b> method will shrink the volume by as much as possible.

Shrink and <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-extend">extend</a> operations are supported only on NTFS and RAW volumes.

Use this method to shrink the file system and volume. If VDS fails to shrink the volume, it stops the operation without shrinking the file system.

Only one shrink or defragmentation operation can be performed at a time on each volume.<b>Windows Server 2008 and Windows Vista:  </b>Only one shrink or defragmentation operation can be performed at a time on a computer.



Implementers must return a pointer to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface for this method, even if the call does not initiate an asynchronous operation.

This method is identical to the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-shrink">IVdsVolume::Shrink</a> method.

You can use the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumeshrink-querymaxreclaimablebytes">IVdsVolumeShrink::QueryMaxReclaimableBytes</a> method to estimate the number of bytes to be reclaimed by the shrink operation. However, <b>QueryMaxReclaimableBytes</b> can return more bytes than are actually available.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-extend">IVdsVolume::Extend</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsvolumeshrink">IVdsVolumeShrink</a>