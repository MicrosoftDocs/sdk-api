---
UID: NF:vds.IVdsVolume.AddPlex
title: IVdsVolume::AddPlex (vds.h)
description: Adds a volume as a plex to the current volume.
helpviewer_keywords: ["AddPlex","AddPlex method [VDS]","AddPlex method [VDS]","IVdsVolume interface","IVdsVolume interface [VDS]","AddPlex method","IVdsVolume.AddPlex","IVdsVolume::AddPlex","base.ivdsvolume_addplex","vds/IVdsVolume::AddPlex"]
old-location: base\ivdsvolume_addplex.htm
tech.root: base
ms.assetid: b463ad74-400d-4100-83ff-3eb98e6a0db4
ms.date: 12/05/2018
ms.keywords: AddPlex, AddPlex method [VDS], AddPlex method [VDS],IVdsVolume interface, IVdsVolume interface [VDS],AddPlex method, IVdsVolume.AddPlex, IVdsVolume::AddPlex, base.ivdsvolume_addplex, vds/IVdsVolume::AddPlex
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
 - IVdsVolume::AddPlex
 - vds/IVdsVolume::AddPlex
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
 - IVdsVolume.AddPlex
---

# IVdsVolume::AddPlex


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Adds a volume as a plex to the 
   current volume.

## -parameters

### -param VolumeId [in]

The GUID of the volume to be added as a plex.

### -param ppAsync [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer, which VDS 
      initializes on return. Callers must release the interface. Use this pointer to cancel, wait for, or query the 
      status of the operation.

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
The plex was added successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_GPT_BOOT_MIRRORED_TO_MBR</b></dt>
<dt>0x80042469L</dt>
</dl>
</td>
<td width="60%">
The boot volume on a GPT disk has been mirrored to an MBR disk. The new plex cannot be used to boot the 
        computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_NOT_ONLINE</b></dt>
<dt>0x8004243DL</dt>
</dl>
</td>
<td width="60%">
The volume is not accessible.

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
The volume is failing or has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_SPANS_DISKS</b></dt>
<dt>0x8004243FL</dt>
</dl>
</td>
<td width="60%">
The volume spans multiple disks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_REQUIRES_CONTIGUOUS_DISK_SPACE</b></dt>
<dt>0x80042440L</dt>
</dl>
</td>
<td width="60%">
The volume consists of multiple extents.

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
The source volume is smaller than the target volume. If the source volume is larger than the target volume, 
        the target volume remains the same size and the operation succeeds.

</td>
</tr>
</table>

## -remarks

This operation is not valid for basic volumes, which have exactly one plex.

Use this method to add a volume as a plex to another volume. For example, a caller can create a volume (volume B), 
    specify volume B as a new plex to an existing volume (volume A), then remove volume B. The new plex of Volume A
    occupies the same disk extents as did volume B.

<div class="alert"><b>Note</b>  VDS attempts to use the same extents, but cannot guarantee this behavior.</div>
<div> </div>
Callers can add a mirrored volume as a new plex to another volume. The resulting volume contains plexes equal in 
    number to the sum of the original volumes.
     

Implementers must return a pointer to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface for 
     this method, regardless of whether the call initiates an asynchronous operation.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>



<a href="/windows/desktop/VDS/volume-plex-object">Volume Plex Object</a>