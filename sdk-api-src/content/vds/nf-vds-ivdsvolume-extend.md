---
UID: NF:vds.IVdsVolume.Extend
title: IVdsVolume::Extend (vds.h)
description: Expands the size of the current volume by adding disk extents to each member of each plex.
helpviewer_keywords: ["Extend","Extend method [VDS]","Extend method [VDS]","IVdsVolume interface","IVdsVolume interface [VDS]","Extend method","IVdsVolume.Extend","IVdsVolume::Extend","base.ivdsvolume_extend","vds/IVdsVolume::Extend"]
old-location: base\ivdsvolume_extend.htm
tech.root: base
ms.assetid: 8f31dd3e-0c06-49fe-8ff2-55cfabe5099e
ms.date: 12/05/2018
ms.keywords: Extend, Extend method [VDS], Extend method [VDS],IVdsVolume interface, IVdsVolume interface [VDS],Extend method, IVdsVolume.Extend, IVdsVolume::Extend, base.ivdsvolume_extend, vds/IVdsVolume::Extend
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
 - IVdsVolume::Extend
 - vds/IVdsVolume::Extend
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
 - IVdsVolume.Extend
---

# IVdsVolume::Extend


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Expands the size of the current 
   volume by adding disk extents to each member of each plex.

## -parameters

### -param pInputDiskArray [in]

Pointer to an array of <a href="/windows/desktop/api/vds/ns-vds-vds_input_disk">VDS_INPUT_DISK</a> structures; 
      one structure for each disk.
      

<div class="alert"><b>Note</b>  Callers should not use a default member index in conjunction with the 
       <b>Extend</b> method, unless the volume has only one 
       plex with only one member.</div>
<div> </div>

### -param lNumberOfDisks [in]

The total number of disks in the volume. Callers can pass zero when the volume plexes contain enough space to 
      extend the volume; <i>pInputDiskArray</i> must be <b>NULL</b>.

### -param ppAsync [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer, which VDS 
      initializes on return. Callers must release the interface. Use this pointer to cancel, wait for, or query the 
      status of the operation. If you call the 
      <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> method on this interface and a success HRESULT value is returned, you must 
      release the interfaces returned in the 
      <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on each interface pointer.
     However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros defined in Winerror.h.

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
The method competed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CANNOT_EXTEND</b></dt>
<dt>0x8004240EL</dt>
</dl>
</td>
<td width="60%">
The volume cannot be extended because the file system on the volume does not support the operation.

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
There is not enough space to extend the volume.

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
</table>

## -remarks

This method extends a simple volume on the same disk, or creates a spanned volume by extending the volume to 
    multiple disks. Callers can extend a volume on a basic disk, however the disk extent must be contiguous with the 
    volume.
   

VDS automatically extends the file system to fit the extended volume size. The file system must support this 
    operation. VDS extends the file system, but not the volume, if a caller fails to specify the extents to be used.
   

Extend and <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumeshrink-shrink">shrink</a> operations are supported only on NTFS and RAW volumes.

VDS applies the following rules when extending a volume: 

<ul>
<li>For simple and spanned plex types, VDS extends the sole member of the plex with any disk extent not already 
      contributing to another plex—whether the extent is on the same disk or not. VDS uses disk extents in the order 
      given by the caller, ignoring the member index of the extent. Unless on a basic disk, VDS can extend the sole 
      member of a plex with any disk extent on the same disk or on a different disk.
     </li>
<li>For striped and striped with parity plex types, VDS assigns an extent to the member of the plex as follows:
      <ul>
<li>The extent goes to the member index specified by the caller.</li>
<li>The extent goes to the member index that occupies the same disk when the caller fails to specify a member ID.</li>
</ul>VDS never assigns an extent to multiple members on the same disk. The caller must specify a member for all 
      extents or none; the caller cannot specify a member for some extents and not for others.</li>
</ul>
When the caller passes <b>NULL</b> for <i>pInputDiskArray</i> and zero for 
    <i>lNumberOfDisks</i>, VDS returns <b>S_FALSE</b> in the async object and 
    <b>S_OK</b> for the method. In this case, <b>S_OK</b> indicates that VDS 
    has started the operation, but the operation is synchronous.
    

Implementers must return a pointer to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface for 
     this method, regardless of whether the call initiates an asynchronous operation.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumeshrink-shrink">IVdsVolumeShrink::Shrink</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_input_disk">VDS_INPUT_DISK</a>