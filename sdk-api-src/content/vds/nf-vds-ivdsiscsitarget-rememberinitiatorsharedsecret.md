---
UID: NF:vds.IVdsIscsiTarget.RememberInitiatorSharedSecret
title: IVdsIscsiTarget::RememberInitiatorSharedSecret
author: windows-sdk-content
description: Communicates the initiator CHAP secret that is used for mutual CHAP authentication when the initiator authenticates the target.
old-location: base\ivdsiscsitarget_rememberinitiatorsharedsecret.htm
old-project: VDS
ms.assetid: 3546f42c-2c30-4819-982d-9c186d9f858e
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsIscsiTarget interface [VDS],RememberInitiatorSharedSecret method, IVdsIscsiTarget.RememberInitiatorSharedSecret, IVdsIscsiTarget::RememberInitiatorSharedSecret, RememberInitiatorSharedSecret, RememberInitiatorSharedSecret method [VDS], RememberInitiatorSharedSecret method [VDS],IVdsIscsiTarget interface, base.ivdsiscsitarget_rememberinitiatorsharedsecret, vds/IVdsIscsiTarget::RememberInitiatorSharedSecret, vdshwprv/IVdsIscsiTarget::RememberInitiatorSharedSecret
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VDS_VOLUME_TYPE
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
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsIscsiTarget::RememberInitiatorSharedSecret


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Communicates the initiator CHAP secret that is used for mutual CHAP authentication when the initiator 
   authenticates the target.


## -parameters




### -param pwszInitiatorName [in]

The string specifying the iSCSI name of the initiator. This parameter is required and cannot be <b>NULL</b>.


### -param pInitiatorSharedSecret [in]


      The address of a <a href="https://msdn.microsoft.com/eab1e2f4-b14e-4336-9b83-5dd7089da2d8">VDS_ISCSI_SHARED_SECRET</a> 
      structure that contains the shared secret.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The shared secret was remembered successfully.

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

        The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0db442c4-6cc1-43b2-8ac8-8b17cadb1101">IVdsIscsiTarget</a>



<a href="https://msdn.microsoft.com/eab1e2f4-b14e-4336-9b83-5dd7089da2d8">VDS_ISCSI_SHARED_SECRET</a>
 

 

