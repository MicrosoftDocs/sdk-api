---
UID: NF:certenroll.IX509PrivateKey.Open
title: IX509PrivateKey::Open
author: windows-driver-content
description: Opens an existing private key.
old-location: security\ix509privatekey_open_method.htm
old-project: SecCertEnroll
ms.assetid: 965e3bf8-22b9-4015-8fb2-102c5f7b1cb5
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IX509PrivateKey interface [Security],Open method, IX509PrivateKey.Open, IX509PrivateKey::Open, Open, Open method [Security], Open method [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::Open, security.ix509privatekey_open_method
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509PrivateKey.Open
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509PrivateKey::Open


## -description


The <b>Open</b> method opens an existing <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>.


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If successful, this method sets the <a href="https://msdn.microsoft.com/7f02b3d7-ab3a-4413-81ac-c626bc79a88c">Opened</a> property. You must call either the <b>Open</b> or <a href="https://msdn.microsoft.com/e8c6564a-6009-437e-9b83-3711e43a7374">Create</a> methods before calling the <a href="https://msdn.microsoft.com/86316966-11d5-42d6-8690-eddfe86f8150">Export</a> method or <a href="https://msdn.microsoft.com/4ebcba09-1fea-4d21-8315-3570eaf6d42d">ExportPublicKey</a> method.

You cannot set the following properties after calling the <b>Open</b> or <a href="https://msdn.microsoft.com/e8c6564a-6009-437e-9b83-3711e43a7374">Create</a> methods. If you wish to specify them, you must do so before calling either of these methods.<ul>
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


The following properties can be set regardless of whether the key is open:<ul>
<li>
<a href="https://msdn.microsoft.com/035615f1-2dc7-47d7-98e4-7b5b0924030f">Certificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/97243031-ef60-467d-ba65-6c7e6432d51f">ParentWindow</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5fa1e5d8-b745-494c-a727-426084fce2a1">SecurityDescriptor</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

