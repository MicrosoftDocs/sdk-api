---
UID: NF:vds.IVdsServiceIscsi.RememberTargetSharedSecret
title: IVdsServiceIscsi::RememberTargetSharedSecret (vds.h)
description: Communicates the CHAP shared secret of a target to the initiator service. This shared secret is used during target login when the target authenticates the initiator.
helpviewer_keywords: ["IVdsServiceIscsi interface [VDS]","RememberTargetSharedSecret method","IVdsServiceIscsi.RememberTargetSharedSecret","IVdsServiceIscsi::RememberTargetSharedSecret","RememberTargetSharedSecret","RememberTargetSharedSecret method [VDS]","RememberTargetSharedSecret method [VDS]","IVdsServiceIscsi interface","base.ivdsserviceiscsi_remembertargetsharedsecret","vds/IVdsServiceIscsi::RememberTargetSharedSecret"]
old-location: base\ivdsserviceiscsi_remembertargetsharedsecret.htm
tech.root: base
ms.assetid: fefe37aa-48c8-4ff4-b302-c6e95c1ffa5e
ms.date: 12/05/2018
ms.keywords: IVdsServiceIscsi interface [VDS],RememberTargetSharedSecret method, IVdsServiceIscsi.RememberTargetSharedSecret, IVdsServiceIscsi::RememberTargetSharedSecret, RememberTargetSharedSecret, RememberTargetSharedSecret method [VDS], RememberTargetSharedSecret method [VDS],IVdsServiceIscsi interface, base.ivdsserviceiscsi_remembertargetsharedsecret, vds/IVdsServiceIscsi::RememberTargetSharedSecret
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
 - IVdsServiceIscsi::RememberTargetSharedSecret
 - vds/IVdsServiceIscsi::RememberTargetSharedSecret
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
 - IVdsServiceIscsi.RememberTargetSharedSecret
---

# IVdsServiceIscsi::RememberTargetSharedSecret


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Communicates the CHAP shared secret of a target to the initiator service. This shared secret is used 
   during target login when the target authenticates the initiator.

## -parameters

### -param targetId [in]

The <b>VDS_OBJECT_ID</b> of the target that has the specified shared secret. This parameter is required and cannot be GUID_NULL.

### -param pTargetSharedSecret [in]

The address of a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_shared_secret">VDS_ISCSI_SHARED_SECRET</a> structure 
      that contains the CHAP shared secret.

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
The shared secret  was remembered successfully.

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
VDS failed to initialize. If an application calls this method before the service finishes initializing, the 
        method is blocked until the initialization completes. If the initialization fails, this error is returned.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-rememberinitiatorsharedsecret">IVdsIscsiTarget::RememberInitiatorSharedSecret</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-setsharedsecret">IVdsIscsiTarget::SetSharedSecret</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsserviceiscsi">IVdsServiceIscsi</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-setinitiatorsharedsecret">IVdsServiceIscsi::SetInitiatorSharedSecret</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_shared_secret">VDS_ISCSI_SHARED_SECRET</a>