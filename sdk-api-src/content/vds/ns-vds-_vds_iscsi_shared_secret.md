---
UID: NS:vds._VDS_ISCSI_SHARED_SECRET
title: "_VDS_ISCSI_SHARED_SECRET"
author: windows-sdk-content
description: Defines a CHAP shared secret.
old-location: base\vds_iscsi_shared_secret.htm
tech.root: vds
ms.assetid: eab1e2f4-b14e-4336-9b83-5dd7089da2d8
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: VDS_ISCSI_SHARED_SECRET, VDS_ISCSI_SHARED_SECRET structure [VDS], _VDS_ISCSI_SHARED_SECRET, base.vds_iscsi_shared_secret, vds/VDS_ISCSI_SHARED_SECRET, vdshwprv/VDS_ISCSI_SHARED_SECRET
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: VDS_ISCSI_SHARED_SECRET
req.redist: VDS 1.1
---

# _VDS_ISCSI_SHARED_SECRET structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

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
<a href="https://msdn.microsoft.com/90f9cf10-a0be-4ed1-8b0c-e6cc46384ba0">IVdsServiceIscsi::SetInitiatorSharedSecret</a> sets the shared secret for an iSCSI initiator. If the <b>pSharedSecret</b> member is <b>NULL</b> and the <b>ulSharedSecretSize</b> member is zero, <b>SetInitiatorSharedSecret</b> clears any existing shared secrets.</li>
<li>
<a href="https://msdn.microsoft.com/2b2eae3d-8ad0-4b68-943b-a42696165543">IVdsIscsiTarget::SetSharedSecret</a> sets the shared secret for an iSCSI target. If the <b>pSharedSecret</b> member is <b>NULL</b> and the <b>ulSharedSecretSize</b> member is zero, <b>SetSharedSecret</b> clears any existing shared secrets.</li>
<li>
<a href="https://msdn.microsoft.com/fefe37aa-48c8-4ff4-b302-c6e95c1ffa5e">IVdsServiceIscsi::RememberTargetSharedSecret</a> tells the initiator to remember the secret of the target.</li>
<li>
<a href="https://msdn.microsoft.com/3546f42c-2c30-4819-982d-9c186d9f858e">IVdsIscsiTarget::RememberInitiatorSharedSecret</a> tells the target to remember the secret of the initiator.</li>
</ul>
For one-way CHAP, the secret is set on the target. The initiator must remember the CHAP secret of the target in order to do a successful login. 

For mutual CHAP, secrets are set on the target and the initiator. To do a successful login, the target and the initiator must remember each other's secrets.




## -see-also




<a href="https://msdn.microsoft.com/3546f42c-2c30-4819-982d-9c186d9f858e">IVdsIscsiTarget::RememberInitiatorSharedSecret</a>



<a href="https://msdn.microsoft.com/2b2eae3d-8ad0-4b68-943b-a42696165543">IVdsIscsiTarget::SetSharedSecret</a>



<a href="https://msdn.microsoft.com/fefe37aa-48c8-4ff4-b302-c6e95c1ffa5e">IVdsServiceIscsi::RememberTargetSharedSecret</a>



<a href="https://msdn.microsoft.com/90f9cf10-a0be-4ed1-8b0c-e6cc46384ba0">IVdsServiceIscsi::SetInitiatorSharedSecret</a>
 

 

