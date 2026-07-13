---
UID: NF:vds.IVdsVolume.RemovePlex
title: IVdsVolume::RemovePlex (vds.h)
description: Removes one or more specified plexes from the current volume, releasing the extents.
helpviewer_keywords: ["IVdsVolume interface [VDS]","RemovePlex method","IVdsVolume.RemovePlex","IVdsVolume::RemovePlex","RemovePlex","RemovePlex method [VDS]","RemovePlex method [VDS]","IVdsVolume interface","base.ivdsvolume_removeplex","vds/IVdsVolume::RemovePlex"]
old-location: base\ivdsvolume_removeplex.htm
tech.root: base
ms.assetid: 724f80e7-4656-4956-aaad-9f778329f139
ms.date: 12/05/2018
ms.keywords: IVdsVolume interface [VDS],RemovePlex method, IVdsVolume.RemovePlex, IVdsVolume::RemovePlex, RemovePlex, RemovePlex method [VDS], RemovePlex method [VDS],IVdsVolume interface, base.ivdsvolume_removeplex, vds/IVdsVolume::RemovePlex
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
 - IVdsVolume::RemovePlex
 - vds/IVdsVolume::RemovePlex
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
 - IVdsVolume.RemovePlex
---

# IVdsVolume::RemovePlex


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Removes one or more 
   specified plexes from the current volume, releasing the extents.

## -parameters

### -param plexId [in]

The GUID of the plex to be removed.

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
The plex was removed successfully.

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
<dt><b>VDS_E_VOLUME_NOT_A_MIRROR</b></dt>
<dt>0x80042445L</dt>
</dl>
</td>
<td width="60%">
The volume is not a mirror.

</td>
</tr>
</table>

## -remarks

This operation cannot remove the last plex of a volume. Instead, use the 
    <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-delete">IVdsVolume::Delete</a> method to remove the last 
    remaining volume (the sole plex). This method is not valid for basic volumes, which have exactly one plex.

VDS does not dismount the volume when it removes a plex.
    

Implementers must return a pointer to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface for 
     this method, regardless of whether the call initiates an asynchronous operation.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsvolume">IVdsVolume</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-delete">IVdsVolume::Delete</a>