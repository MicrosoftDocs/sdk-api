---
UID: NF:vds.IVdsVolume.Shrink
title: IVdsVolume::Shrink (vds.h)
description: Reduces the size of the volume and all plexes, and returns the released extents to free space.
helpviewer_keywords: ["IVdsVolume interface [VDS]","Shrink method","IVdsVolume.Shrink","IVdsVolume::Shrink","Shrink","Shrink method [VDS]","Shrink method [VDS]","IVdsVolume interface","base.ivdsvolume_shrink","vds/IVdsVolume::Shrink"]
old-location: base\ivdsvolume_shrink.htm
tech.root: base
ms.assetid: 63ac6ef9-0e84-40ed-a302-4f32316a41cc
ms.date: 12/05/2018
ms.keywords: IVdsVolume interface [VDS],Shrink method, IVdsVolume.Shrink, IVdsVolume::Shrink, Shrink, Shrink method [VDS], Shrink method [VDS],IVdsVolume interface, base.ivdsvolume_shrink, vds/IVdsVolume::Shrink
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
 - IVdsVolume::Shrink
 - vds/IVdsVolume::Shrink
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
 - IVdsVolume.Shrink
---

# IVdsVolume::Shrink


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Reduces the size of the volume 
   and all plexes, and returns the released extents to free space.

## -parameters

### -param ullNumberOfBytesToRemove [in]

The size of the reduction in bytes.

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
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
        method to restore the cache.
       

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
<dt><b>VDS_E_SHRINK_SIZE_TOO_BIG</b></dt>
<dt>0x80042574L</dt>
</dl>
</td>
<td width="60%">
The specified shrink size is too large and will cause the volume to be smaller than the minimum volume size.

</td>
</tr>
</table>

## -remarks

This method is a wrapper for the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumeshrink-shrink">IVdsVolumeShrink::Shrink</a> method. If you call <b>IVdsVolume::Shrink</b>, the value of the <i>uNumberOfBytesToRemove</i> parameter is used for the <i>ullDesiredNumberOfReclaimableBytes</i> and <i>ullMinNumberOfReclaimableBytes</i> parameters of <b>IVdsVolumeShrink::Shrink</b>.

Shrink and <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-extend">extend</a> operations are supported only on NTFS and RAW volumes.

Use this method to shrink the file system and volume. If VDS fails to shrink the volume, it stops the operation 
    without shrinking the file system.
   

Only one shrink or defragmentation operation can be performed at a time on each volume.<b>Windows Server 2008 and Windows Vista:  </b>Only one shrink or defragmentation operation can be performed at a time on a computer.



If <i>uNumberOfBytesToRemove</i> is zero, the method fails. Otherwise, VDS rounds 
    <i>uNumberOfBytesToRemove</i> to a multiple of the file system cluster size.
     
     
      

Implementers must return a pointer to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface for 
      this method, even if the call does not initiate an asynchronous operation.

You can use the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumeshrink-querymaxreclaimablebytes">IVdsVolumeShrink::QueryMaxReclaimableBytes</a> method to estimate the number of bytes to be reclaimed by the shrink operation. However, <b>QueryMaxReclaimableBytes</b> can return more bytes than are actually available.
## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-extend">IVdsVolume::Extend</a>