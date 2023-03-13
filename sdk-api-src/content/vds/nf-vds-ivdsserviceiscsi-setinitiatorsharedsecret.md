---
UID: NF:vds.IVdsServiceIscsi.SetInitiatorSharedSecret
title: IVdsServiceIscsi::SetInitiatorSharedSecret (vds.h)
description: Sets the initiator CHAP shared secret that is used for mutual CHAP authentication when the initiator authenticates the target.
helpviewer_keywords: ["IVdsServiceIscsi interface [VDS]","SetInitiatorSharedSecret method","IVdsServiceIscsi.SetInitiatorSharedSecret","IVdsServiceIscsi::SetInitiatorSharedSecret","SetInitiatorSharedSecret","SetInitiatorSharedSecret method [VDS]","SetInitiatorSharedSecret method [VDS]","IVdsServiceIscsi interface","base.ivdsserviceiscsi_setinitiatorsharedsecret","vds/IVdsServiceIscsi::SetInitiatorSharedSecret"]
old-location: base\ivdsserviceiscsi_setinitiatorsharedsecret.htm
tech.root: base
ms.assetid: 90f9cf10-a0be-4ed1-8b0c-e6cc46384ba0
ms.date: 12/05/2018
ms.keywords: IVdsServiceIscsi interface [VDS],SetInitiatorSharedSecret method, IVdsServiceIscsi.SetInitiatorSharedSecret, IVdsServiceIscsi::SetInitiatorSharedSecret, SetInitiatorSharedSecret, SetInitiatorSharedSecret method [VDS], SetInitiatorSharedSecret method [VDS],IVdsServiceIscsi interface, base.ivdsserviceiscsi_setinitiatorsharedsecret, vds/IVdsServiceIscsi::SetInitiatorSharedSecret
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
 - IVdsServiceIscsi::SetInitiatorSharedSecret
 - vds/IVdsServiceIscsi::SetInitiatorSharedSecret
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
 - IVdsServiceIscsi.SetInitiatorSharedSecret
---

# IVdsServiceIscsi::SetInitiatorSharedSecret


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the initiator CHAP shared secret that is used for mutual CHAP authentication when the initiator 
   authenticates the target.

## -parameters

### -param pInitiatorSharedSecret [in]

The address of a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_shared_secret">VDS_ISCSI_SHARED_SECRET</a> 
      structure that contains the shared secret. If the <b>pSharedSecret</b> member  is <b>NULL</b> and the <b>ulSharedSecretSize</b> is zero, the <b>SetInitiatorSharedSecret</b> method  clears   any existing secret. If this parameter is <b>NULL</b> and the <i>targetId</i> 
      parameter is not <b>GUID_NULL</b>, <b>SetInitiatorSharedSecret</b> clears the association between the initiator and the target.

### -param targetId [in]

The <b>VDS_OBJECT_ID</b> of the target. This parameter is set to 
      <b>GUID_NULL</b> if the shared secret is not to be target-specific.

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
The shared secret  was set successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
VDS failed to initialize. If an application calls this method before the service finishes initializing, 
        the method is blocked until the initialization completes. If the initialization fails, this error is returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_TARGET_SPECIFIC_NOT_SUPPORTED</b></dt>
<dt>0x80042706L</dt>
</dl>
</td>
<td width="60%">
The initiator service does not support setting target-specific shared secrets.

</td>
</tr>
</table>

## -remarks

An initiator may support setting a different CHAP shared secret for each target.

There is no way to determine programmatically whether an initiator   supports target-specific secrets. If the call to <b>SetInitiatorSharedSecret</b> returns VDS_E_TARGET_SPECIFIC_NOT_SUPPORTED, call the method again, setting the <i>targetId</i> parameter to GUID_NULL.

The Microsoft iSCSI Software Initiator does not support setting target-specific secrets.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-rememberinitiatorsharedsecret">IVdsIscsiTarget::RememberInitiatorSharedSecret</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-setsharedsecret">IVdsIscsiTarget::SetSharedSecret</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsserviceiscsi">IVdsServiceIscsi</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-remembertargetsharedsecret">IVdsServiceIscsi::RememberTargetSharedSecret</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_shared_secret">VDS_ISCSI_SHARED_SECRET</a>