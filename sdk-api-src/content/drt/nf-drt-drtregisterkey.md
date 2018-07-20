---
UID: NF:drt.DrtRegisterKey
title: DrtRegisterKey function
author: windows-sdk-content
description: The DrtRegisterKey function registers a key in the DRT.
old-location: p2p\drtregisterkey.htm
old-project: p2psdk
ms.assetid: 9aa1ee16-648d-4769-a464-4659dea14dba
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: DrtRegisterKey, DrtRegisterKey function [Peer Networking], drt/DrtRegisterKey, p2p.drtregisterkey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DRT_REGISTRATION_STATE, *PDRT_REGISTRATION_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtRegisterKey
product: Windows
targetos: Windows
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
---

# DrtRegisterKey function


## -description


The <b>DrtRegisterKey</b> function registers a key in the DRT. 


## -parameters




### -param hDrt [in]

A pointer to a handle returned by the <a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a> function.


### -param pRegistration [in]

A pointer to a handle to the <a href="https://msdn.microsoft.com/1b5fea2c-c1df-4639-8f62-e62d8a09b1f5">DRT_REGISTRATION</a> structure.


### -param pvKeyContext [in, optional]

Pointer to the context data associated with the key in the DRT. This data is passed to the key-specific functions of the security provider.


### -param phKeyRegistration [out]

Pointer to a handle for a key that has been registered.


## -returns



This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li><i>pRegistration</i> is <b>NULL</b></li>
<li>The <b>cb</b> value  of the <b>appData</b> member of the <a href="https://msdn.microsoft.com/1b5fea2c-c1df-4639-8f62-e62d8a09b1f5">DRT_REGISTRATION</a> structure is too large (ie. less than 1).</li>
<li>The <b>cb</b> value  of the <b>appData</b> member of the    <a href="https://msdn.microsoft.com/1b5fea2c-c1df-4639-8f62-e62d8a09b1f5">DRT_REGISTRATION</a> structure is too large (ie. more than 5120).</li>
<li>The <b>pb</b> value  of the <b>key</b> member   of the <a href="https://msdn.microsoft.com/1b5fea2c-c1df-4639-8f62-e62d8a09b1f5">DRT_REGISTRATION</a> structure is <b>NULL</b>.</li>
<li><i>phKeyRegistration</i> is <b>NULL</b></li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hDrt</i> is an invalid handle or <i>phKeyRegistration</i> is an invalid handle

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_KEY_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The size of cb value of the  key member of the DRT_REGISTRATION structure  is not equal to 256 bits or the <b>pb</b> value  of the <b>key</b> member   of the <a href="https://msdn.microsoft.com/1b5fea2c-c1df-4639-8f62-e62d8a09b1f5">DRT_REGISTRATION</a> structure is <b>NULL</b>..

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_FAULTED</b></dt>
</dl>
</td>
<td width="60%">
The DRT cloud is in the faulted state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_DUPLICATE_KEY</b></dt>
</dl>
</td>
<td width="60%">
The key is already registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_CERT_CHAIN</b></dt>
</dl>
</td>
<td width="60%">
The provided certification chain is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_CAPABILITY_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
Supplied certificate provider is not AES capable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_KEY</b></dt>
</dl>
</td>
<td width="60%">
Supplied key does not match generated key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_NO_DEST_ADDRESSES</b></dt>
</dl>
</td>
<td width="60%">
Valid address not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_SHUTTING_DOWN</b></dt>
</dl>
</td>
<td width="60%">
Transport is shutting down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_TRANSPORT_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
Transport provider is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORTPROVIDER_NOT_ATTACHED</b></dt>
</dl>
</td>
<td width="60%">
Transport is not attached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_SECURITYPROVIDER_NOT_ATTACHED</b></dt>
</dl>
</td>
<td width="60%">
Security provider is not attached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_NOT_BOUND</b></dt>
</dl>
</td>
<td width="60%">
Transport is not currently bound.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li>The GlobalControl.HandleTable is <b>NULL</b>.</li>
<li>The cloud is shutting down.</li>
<li>The DRT is shutting down.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unexpected fatal error has occurred.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  <b>DrtRegisterKey</b> may also surface errors from underlying calls to <a href="https://msdn.microsoft.com/c0b7c1c8-aa42-4d40-a7f7-99c0821c8977">CryptGetProvParam</a>, <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a>, <a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>, <a href="https://msdn.microsoft.com/5e4d8cae-1096-491f-9a04-92b7e9c020bb">CertAddCertificateContextToStore</a>, <a href="https://msdn.microsoft.com/074666a7-369c-43bc-97d9-3bcc9703976b">CryptContextAddRef</a>, <a href="https://msdn.microsoft.com/53c9aec9-701d-4c21-9814-d344a8dde0c1">CryptAcquireCertificatePrivateKey</a>, <a href="https://msdn.microsoft.com/5cc818d7-b079-4962-aabc-fc512d4e92ac">CertSaveStore</a>, <a href="https://msdn.microsoft.com/038aeca6-d7b7-4f74-ac69-4536c2e5118b">WSAIoctl</a>, <a href="https://msdn.microsoft.com/c73f2499-75e9-4146-ae4c-0e949206ea37">CryptImportPublicKeyInfoEx2</a>, <a href="https://msdn.microsoft.com/7404e37a-d7c6-49ed-b951-6081dd2b921a">NCryptSignHash</a>, <a href="https://msdn.microsoft.com/c5ab5b4c-dc0c-416b-aa9e-b939398cfa6d">CertEnumCertificatesInStore</a>, <a href="https://msdn.microsoft.com/5c62ca3a-843e-41a7-9340-41785fbb15f4">BCryptGetProperty</a>, <a href="https://msdn.microsoft.com/7c6cee3a-f2c5-46f3-8cfe-984316f323d9">BCryptGenRandom</a>, <a href="https://msdn.microsoft.com/c55d714f-f47e-4ddf-97b9-985c0441bb2d">BCryptGenerateSymmetricKey</a> and <a href="https://msdn.microsoft.com/69fe4530-4b7c-40db-a85c-f9dc458735e7">BCryptEncrypt</a>.</div>
<div> </div>



## -remarks



 A node can register keys while in the <b>DRT_ACTIVE</b>, <b>DRT_ALONE</b>, or <b>DRT_NO_NETWORK</b> state.   However, keys registered in <b>DRT_ALONE</b> and <b>DRT_NO_NETWORK</b> states can only be recognized by other DRTs after the local node has transitioned to <b>DRT_ACTIVE</b>.

 To update an existing key, an application must first deregister the key with <a href="https://msdn.microsoft.com/cf8f877b-44a8-4153-bf02-0b0061bc53d2">DrtUnregisterKey</a> before calling <b>DrtRegisterKey</b> to register the updated key.




## -see-also




<a href="https://msdn.microsoft.com/1b5fea2c-c1df-4639-8f62-e62d8a09b1f5">DRT_REGISTRATION</a>



<a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a>



<a href="https://msdn.microsoft.com/cf8f877b-44a8-4153-bf02-0b0061bc53d2">DrtUnregisterKey</a>
 

 

