---
UID: NF:vds.IVdsIscsiTarget.RememberInitiatorSharedSecret
title: IVdsIscsiTarget::RememberInitiatorSharedSecret (vds.h)
description: The RememberInitiatorSharedSecret method (vds.h) communicates the initiator CHAP secret that the initiator used for mutual CHAP authentication of the target.
helpviewer_keywords: ["IVdsIscsiTarget interface [VDS]","RememberInitiatorSharedSecret method","IVdsIscsiTarget.RememberInitiatorSharedSecret","IVdsIscsiTarget::RememberInitiatorSharedSecret","RememberInitiatorSharedSecret","RememberInitiatorSharedSecret method [VDS]","RememberInitiatorSharedSecret method [VDS]","IVdsIscsiTarget interface","base.ivdsiscsitarget_rememberinitiatorsharedsecret","vds/IVdsIscsiTarget::RememberInitiatorSharedSecret","vdshwprv/IVdsIscsiTarget::RememberInitiatorSharedSecret"]
old-location: base\ivdsiscsitarget_rememberinitiatorsharedsecret.htm
tech.root: base
ms.assetid: 3546f42c-2c30-4819-982d-9c186d9f858e
ms.date: 08/05/2022
ms.keywords: IVdsIscsiTarget interface [VDS],RememberInitiatorSharedSecret method, IVdsIscsiTarget.RememberInitiatorSharedSecret, IVdsIscsiTarget::RememberInitiatorSharedSecret, RememberInitiatorSharedSecret, RememberInitiatorSharedSecret method [VDS], RememberInitiatorSharedSecret method [VDS],IVdsIscsiTarget interface, base.ivdsiscsitarget_rememberinitiatorsharedsecret, vds/IVdsIscsiTarget::RememberInitiatorSharedSecret, vdshwprv/IVdsIscsiTarget::RememberInitiatorSharedSecret
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsIscsiTarget::RememberInitiatorSharedSecret
 - vds/IVdsIscsiTarget::RememberInitiatorSharedSecret
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
 - IVdsIscsiTarget.RememberInitiatorSharedSecret
---

# IVdsIscsiTarget::RememberInitiatorSharedSecret


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Communicates the initiator CHAP secret that is used for mutual CHAP authentication when the initiator 
   authenticates the target.

## -parameters

### -param pwszInitiatorName [in]

The string specifying the iSCSI name of the initiator. This parameter is required and cannot be <b>NULL</b>.

### -param pInitiatorSharedSecret [in]

The address of a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_shared_secret">VDS_ISCSI_SHARED_SECRET</a> 
      structure that contains the shared secret.

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
The shared secret was remembered successfully.

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
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsitarget">IVdsIscsiTarget</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_shared_secret">VDS_ISCSI_SHARED_SECRET</a>
