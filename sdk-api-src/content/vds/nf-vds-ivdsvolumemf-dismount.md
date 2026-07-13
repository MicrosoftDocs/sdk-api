---
UID: NF:vds.IVdsVolumeMF.Dismount
title: IVdsVolumeMF::Dismount (vds.h)
description: Dismounts a mounted volume.
helpviewer_keywords: ["Dismount","Dismount method [VDS]","Dismount method [VDS]","IVdsVolumeMF interface","IVdsVolumeMF interface [VDS]","Dismount method","IVdsVolumeMF.Dismount","IVdsVolumeMF::Dismount","base.ivdsvolumemf_dismount","vds/IVdsVolumeMF::Dismount"]
old-location: base\ivdsvolumemf_dismount.htm
tech.root: base
ms.assetid: 1ef5a1e6-0e41-4077-9ae8-fe266f2623cc
ms.date: 12/05/2018
ms.keywords: Dismount, Dismount method [VDS], Dismount method [VDS],IVdsVolumeMF interface, IVdsVolumeMF interface [VDS],Dismount method, IVdsVolumeMF.Dismount, IVdsVolumeMF::Dismount, base.ivdsvolumemf_dismount, vds/IVdsVolumeMF::Dismount
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
 - IVdsVolumeMF::Dismount
 - vds/IVdsVolumeMF::Dismount
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
 - IVdsVolumeMF.Dismount
---

# IVdsVolumeMF::Dismount


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Dismounts a mounted volume.

## -parameters

### -param bForce [in]

If <b>TRUE</b>, the volume is dismounted even if it is in use; otherwise, the operation fails if the volume is in use.

### -param bPermanent [in]

If <b>TRUE</b>, the volume remains dismounted until an access path is added.

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
<dt><b>VDS_E_VOLUME_TEMPORARILY_DISMOUNTED</b></dt>
<dt>0x8004245CL</dt>
</dl>
</td>
<td width="60%">
The volume is already dismounted. 

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
The volume cannot be dismounted. It does not support the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_PERMANENTLY_DISMOUNTED</b></dt>
<dt>0x8004245DL</dt>
</dl>
</td>
<td width="60%">
The volume is already dismounted. It cannot be dismounted temporarily until it becomes mountable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_HAS_PATH</b></dt>
<dt>0x8004245EL</dt>
</dl>
</td>
<td width="60%">
The volume cannot be dismounted because it still has an access path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DEVICE_IN_USE</b></dt>
<dt>0x80042413L</dt>
</dl>
</td>
<td width="60%">
The volume is in use and cannot be dismounted.

</td>
</tr>
</table>

## -remarks

 To mount a volume, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-mount">Mount</a> method.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvolumemf">IVdsVolumeMF</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-mount">IVdsVolumeMF::Mount</a>