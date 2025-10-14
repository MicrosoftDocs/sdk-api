---
UID: NF:vdshwprv.IVdsIscsiTarget.SetSharedSecret
title: IVdsIscsiTarget::SetSharedSecret (vdshwprv.h)
description: The IVdsIscsiTarget::SetSharedSecret method sets the target CHAP shared secret that is used for CHAP authentication when the target authenticates the initiator.
helpviewer_keywords: ["IVdsIscsiTarget interface [VDS]","SetSharedSecret method","IVdsIscsiTarget.SetSharedSecret","IVdsIscsiTarget::SetSharedSecret","SetSharedSecret","SetSharedSecret method [VDS]","SetSharedSecret method [VDS]","IVdsIscsiTarget interface","base.ivdsiscsitarget_setsharedsecret","vds/IVdsIscsiTarget::SetSharedSecret","vdshwprv/IVdsIscsiTarget::SetSharedSecret"]
old-location: base\ivdsiscsitarget_setsharedsecret.htm
tech.root: base
ms.assetid: 2b2eae3d-8ad0-4b68-943b-a42696165543
ms.date: 08/08/2022
ms.keywords: IVdsIscsiTarget interface [VDS],SetSharedSecret method, IVdsIscsiTarget.SetSharedSecret, IVdsIscsiTarget::SetSharedSecret, SetSharedSecret, SetSharedSecret method [VDS], SetSharedSecret method [VDS],IVdsIscsiTarget interface, base.ivdsiscsitarget_setsharedsecret, vds/IVdsIscsiTarget::SetSharedSecret, vdshwprv/IVdsIscsiTarget::SetSharedSecret
req.header: vdshwprv.h
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsIscsiTarget::SetSharedSecret
 - vdshwprv/IVdsIscsiTarget::SetSharedSecret
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
 - IVdsIscsiTarget.SetSharedSecret
---

# IVdsIscsiTarget::SetSharedSecret


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the target CHAP shared secret that is used for CHAP authentication when the target authenticates the 
   initiator.

## -parameters

### -param pTargetSharedSecret [in]

The address of an <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_shared_secret">VDS_ISCSI_SHARED_SECRET</a> 
      structure that contains the shared secret. If the <b>pSharedSecret</b> member  is <b>NULL</b> and the <b>ulSharedSecretSize</b> is zero, the <b>SetSharedSecret</b> method  clears   any existing secret.

### -param pwszInitiatorName [in]

The string specifying the iSCSI name to which the shared secret is to be associated, if the secret is 
      initiator-specific. The value passed is used as the CHAP name. If the address is <b>NULL</b> 
      the changes apply to the default secret for all initiators.

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
The shared secret was set successfully.

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
The cache of the provider is corrupted. This indicates a software or communication problem inside a 
        provider that caches information about the attached devices. The caller can use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
        method to restore the cache.

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
The target object is no longer present.

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
This operation or combination of parameters is not supported by this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIATOR_SPECIFIC_NOT_SUPPORTED</b></dt>
<dt>0x80042707L</dt>
</dl>
</td>
<td width="60%">
The target does not support initiator-specific shared secrets.

</td>
</tr>
</table>

## -remarks

The hardware provider must configure the subsystem itself to change the target shared secret. Secrets that are used for 
    security are not persisted by VDS nor should they be persisted by the hardware providers on the local computer. 
    The hardware provider should transmit the secret to the subsystem in a secure manner, and the subsystem is 
    responsible for persisting it.

Some iSCSI targets may support setting a different CHAP shared secret for each initiator. If a target does not support initiator-specific secrets,  the call to <b>SetSharedSecret</b> returns VDS_E_INITIATOR_SPECIFIC_NOT_SUPPORTED.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsitarget">IVdsIscsiTarget</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-rememberinitiatorsharedsecret">IVdsIscsiTarget::RememberInitiatorSharedSecret</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-setsharedsecret">IVdsIscsiTarget::SetSharedSecret</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-setinitiatorsharedsecret">IVdsServiceIscsi::SetInitiatorSharedSecret</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_shared_secret">VDS_ISCSI_SHARED_SECRET</a>
