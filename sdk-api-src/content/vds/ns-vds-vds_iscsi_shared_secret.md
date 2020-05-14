---
UID: NS:vds._VDS_ISCSI_SHARED_SECRET
title: VDS_ISCSI_SHARED_SECRET (vds.h)
description: Defines a CHAP shared secret.helpviewer_keywords: ["VDS_ISCSI_SHARED_SECRET","VDS_ISCSI_SHARED_SECRET structure [VDS]","_VDS_ISCSI_SHARED_SECRET","base.vds_iscsi_shared_secret","vds/VDS_ISCSI_SHARED_SECRET","vdshwprv/VDS_ISCSI_SHARED_SECRET"]
old-location: base\vds_iscsi_shared_secret.htm
tech.root: VDS
ms.assetid: eab1e2f4-b14e-4336-9b83-5dd7089da2d8
ms.date: 12/05/2018
ms.keywords: VDS_ISCSI_SHARED_SECRET, VDS_ISCSI_SHARED_SECRET structure [VDS], _VDS_ISCSI_SHARED_SECRET, base.vds_iscsi_shared_secret, vds/VDS_ISCSI_SHARED_SECRET, vdshwprv/VDS_ISCSI_SHARED_SECRET
f1_keywords:
- vds/VDS_ISCSI_SHARED_SECRET
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vds.h
- VdsHwPrv.h
api_name:
- VDS_ISCSI_SHARED_SECRET
targetos: Windows
req.typenames: VDS_ISCSI_SHARED_SECRET
req.redist: VDS 1.1
ms.custom: 19H1
---

# VDS_ISCSI_SHARED_SECRET structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines a CHAP shared secret.
   


## -struct-fields




### -field pSharedSecret

A pointer to an array of bytes that contains the CHAP shared secret. If a shared secret is not necessary, this parameter should be <b>NULL</b>.
      


### -field ulSharedSecretSize

The number of bytes in the array that the <b>pSharedSecret</b> member points to. If the <b>pSharedSecret</b> member is <b>NULL</b>, this parameter must be zero. If  <b>pSharedSecret</b> is not <b>NULL</b>, this parameter must be greater than or equal to 12 and less than or equal to 16.


## -remarks



This structure is used by the following methods: 

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-setinitiatorsharedsecret">IVdsServiceIscsi::SetInitiatorSharedSecret</a> sets the shared secret for an iSCSI initiator. If the <b>pSharedSecret</b> member is <b>NULL</b> and the <b>ulSharedSecretSize</b> member is zero, <b>SetInitiatorSharedSecret</b> clears any existing shared secrets.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-setsharedsecret">IVdsIscsiTarget::SetSharedSecret</a> sets the shared secret for an iSCSI target. If the <b>pSharedSecret</b> member is <b>NULL</b> and the <b>ulSharedSecretSize</b> member is zero, <b>SetSharedSecret</b> clears any existing shared secrets.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-remembertargetsharedsecret">IVdsServiceIscsi::RememberTargetSharedSecret</a> tells the initiator to remember the secret of the target.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-rememberinitiatorsharedsecret">IVdsIscsiTarget::RememberInitiatorSharedSecret</a> tells the target to remember the secret of the initiator.</li>
</ul>
For one-way CHAP, the secret is set on the target. The initiator must remember the CHAP secret of the target in order to do a successful login. 

For mutual CHAP, secrets are set on the target and the initiator. To do a successful login, the target and the initiator must remember each other's secrets.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-rememberinitiatorsharedsecret">IVdsIscsiTarget::RememberInitiatorSharedSecret</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-setsharedsecret">IVdsIscsiTarget::SetSharedSecret</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-remembertargetsharedsecret">IVdsServiceIscsi::RememberTargetSharedSecret</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceiscsi-setinitiatorsharedsecret">IVdsServiceIscsi::SetInitiatorSharedSecret</a>
 

 

