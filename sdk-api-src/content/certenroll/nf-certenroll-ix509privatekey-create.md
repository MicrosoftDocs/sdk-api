---
UID: NF:certenroll.IX509PrivateKey.Create
title: IX509PrivateKey::Create
author: windows-sdk-content
description: Creates an asymmetric private key.
old-location: security\ix509privatekey_create_method.htm
old-project: seccertenroll
ms.assetid: e8c6564a-6009-437e-9b83-3711e43a7374
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Create, Create method [Security], Create method [Security],IX509PrivateKey interface, IX509PrivateKey interface [Security],Create method, IX509PrivateKey.Create, IX509PrivateKey::Create, certenroll/IX509PrivateKey::Create, security.ix509privatekey_create_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PrivateKey.Create
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509PrivateKey::Create


## -description


The <b>Create</b> method creates an asymmetric  <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_BUSY)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The CSP handle is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_FILE_EXISTS)</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key already exists.

</td>
</tr>
</table>
 




## -remarks



If you do not set the <a href="https://msdn.microsoft.com/8bf6e62d-9ecf-4eee-9652-f04d2010b4f7">CspStatus</a>, the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915743">ProviderName</a>, or <a href="https://msdn.microsoft.com/5f4d2e29-8c02-4d9c-a3a6-15c222650c3e">ProviderType</a> properties, this method uses the default provider, key size, and <a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a> values  when creating the key. On a new operating system installation, for example,  Microsoft Enhanced Cryptographic Provider v1.0 is the default provider.

If you do not set the <a href="https://msdn.microsoft.com/1d56fa7e-8113-461d-a4f0-ebc048fbcb49">ContainerName</a> property, this method automatically generates a name. The generated name includes a GUID and,  if the <a href="https://msdn.microsoft.com/af5a30dd-4707-4b38-bf6b-b971d854d5b0">ContainerNamePrefix</a> property is not set, a prefix of "lp-". If the provider is a smart card provider, the generated name will not exceed the <a href="https://msdn.microsoft.com/2508786f-0892-4ece-bbef-bd8ed9c81eee">MaxKeyContainerNameLength</a> value specified by the provider. If the generated name initially exceeds this value, it is truncated to forty characters.

You cannot set the following properties after calling the <b>Create</b> or <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> methods. If you wish to specify them, you must do so before calling either of these methods.<ul>
<li>
<a href="https://msdn.microsoft.com/40d2eae1-733a-4e5b-bb15-71301d73f438">Algorithm</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d56fa7e-8113-461d-a4f0-ebc048fbcb49">ContainerName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/af5a30dd-4707-4b38-bf6b-b971d854d5b0">ContainerNamePrefix</a>
</li>
<li>
<a href="https://msdn.microsoft.com/81cf4689-0cd6-4185-9242-ef26de9161a1">CspInformations</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8bf6e62d-9ecf-4eee-9652-f04d2010b4f7">CspStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0ef32207-1fb0-49a2-95cf-353f907f3fc6">Existing</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e3f04252-fe49-48fb-9e77-8a05031abf5f">ExportPolicy</a>
</li>
<li>
<a href="https://msdn.microsoft.com/93cd4fe0-5a08-4936-bbb0-6a723027e8c7">FriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/39d8b9ac-ebbd-4bd8-8d5e-a4b28595b030">KeyProtection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e983c95b-6b3a-4e27-8a23-ef9051b11a16">KeyUsage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/53a93aea-4435-4e04-9bd1-6356446aaefc">LegacyCsp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/de25aa05-bd65-49a6-9cd1-e18522c9e190">Length</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bdc3278e-3b5a-4ad0-9e9b-9639a2db4040">MachineContext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn915743">ProviderName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5f4d2e29-8c02-4d9c-a3a6-15c222650c3e">ProviderType</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d81fad8a-767d-48c8-874a-c34843600b13">Pin</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1c9bb81a-c91b-42b9-a44c-de1ae5b68af6">ReaderName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4f61a513-620c-48c4-b9dd-032b13a9f654">Silent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a1a6a474-5ffa-4b68-b84f-b0c9bea30ee5">UIContextMessage</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

