---
UID: NF:vdshwprv.IVdsIscsiTarget.SetSharedSecret
title: IVdsIscsiTarget::SetSharedSecret
author: windows-driver-content
description: Sets the target CHAP shared secret that is used for CHAP authentication when the target authenticates the initiator.
old-location: base\ivdsiscsitarget_setsharedsecret.htm
old-project: VDS
ms.assetid: 2b2eae3d-8ad0-4b68-943b-a42696165543
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IVdsIscsiTarget interface [VDS],SetSharedSecret method, IVdsIscsiTarget.SetSharedSecret, IVdsIscsiTarget::SetSharedSecret, SetSharedSecret, SetSharedSecret method [VDS], SetSharedSecret method [VDS],IVdsIscsiTarget interface, base.ivdsiscsitarget_setsharedsecret, vds/IVdsIscsiTarget::SetSharedSecret, vdshwprv/IVdsIscsiTarget::SetSharedSecret
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsIscsiTarget.SetSharedSecret
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsIscsiTarget::SetSharedSecret


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Sets the target CHAP shared secret that is used for CHAP authentication when the target authenticates the 
   initiator.


## -parameters




### -param pTargetSharedSecret [in]

The address of an <a href="https://msdn.microsoft.com/eab1e2f4-b14e-4336-9b83-5dd7089da2d8">VDS_ISCSI_SHARED_SECRET</a> 
      structure that contains the shared secret. If the <b>pSharedSecret</b> member  is <b>NULL</b> and the <b>ulSharedSecretSize</b> is zero, the <b>SetSharedSecret</b> method  clears   any existing secret. 


### -param pwszInitiatorName [in]

The string specifying the iSCSI name to which the shared secret is to be associated, if the secret is 
      initiator-specific. The value passed is used as the CHAP name. If the address is <b>NULL</b> 
      the changes apply to the default secret for all initiators.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The shared secret was set successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a 
        provider that caches information about the attached devices. The caller can use the 
        <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> 
        method to restore the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_OBJECT_DELETED</b></b></dt>
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
<dt><b><b>VDS_E_NOT_SUPPORTED</b></b></dt>
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
<dt><b><b>VDS_E_INITIATOR_SPECIFIC_NOT_SUPPORTED</b></b></dt>
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




<a href="https://msdn.microsoft.com/0db442c4-6cc1-43b2-8ac8-8b17cadb1101">IVdsIscsiTarget</a>



<a href="https://msdn.microsoft.com/3546f42c-2c30-4819-982d-9c186d9f858e">IVdsIscsiTarget::RememberInitiatorSharedSecret</a>



<a href="https://msdn.microsoft.com/2b2eae3d-8ad0-4b68-943b-a42696165543">IVdsIscsiTarget::SetSharedSecret</a>



<a href="https://msdn.microsoft.com/90f9cf10-a0be-4ed1-8b0c-e6cc46384ba0">IVdsServiceIscsi::SetInitiatorSharedSecret</a>



<a href="https://msdn.microsoft.com/eab1e2f4-b14e-4336-9b83-5dd7089da2d8">VDS_ISCSI_SHARED_SECRET</a>
 

 

