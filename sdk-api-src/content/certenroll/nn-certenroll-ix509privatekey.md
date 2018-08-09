---
UID: NN:certenroll.IX509PrivateKey
title: IX509PrivateKey
author: windows-sdk-content
description: Represents an asymmetric private key that can be used for encryption, signing, and key agreement.
old-location: security\ix509privatekey.htm
old-project: seccertenroll
ms.assetid: 72612ea4-ed45-46ac-9dad-614a9a754d83
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509PrivateKey, IX509PrivateKey interface [Security], IX509PrivateKey interface [Security],described, certenroll/IX509PrivateKey, security.ix509privatekey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IX509PrivateKey
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509PrivateKey interface


## -description


The <b>IX509PrivateKey</b> interface represents an asymmetric private key that can be used for encryption, signing, and key agreement.  Private keys are referenced in the following objects:<ul>
<li>
<a href="https://msdn.microsoft.com/1c35c2f0-8e79-4031-bae2-2be081f3c8dd">ICertPropertyKeyProvInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/146a1925-4de6-492c-8014-612c65bd7270">ISignerCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b42111e9-e39e-4192-9aba-47403fb627dc">IX509AttributeArchiveKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509PrivateKey</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509PrivateKey</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509PrivateKey</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Releases the handle of the cryptographic service provider (CSP) or the handle of the Cryptography API: Next Generation (CNG) key storage provider (KSP).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8c6564a-6009-437e-9b83-3711e43a7374">Create</a>
</td>
<td align="left" width="63%">
Creates an asymmetric  private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f319e20-d993-480e-846d-0912bb854415">Delete</a>
</td>
<td align="left" width="63%">
Releases the handle of the CSP or KSP and deletes the key from disk or smart card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86316966-11d5-42d6-8690-eddfe86f8150">Export</a>
</td>
<td align="left" width="63%">
Copies the private key to a byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ebcba09-1fea-4d21-8315-3570eaf6d42d">ExportPublicKey</a>
</td>
<td align="left" width="63%">
Exports the public key portion of the asymmetric key pair.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33e335e2-9c3f-4aa1-a393-db0ee8095b64">Import</a>
</td>
<td align="left" width="63%">
Imports an existing private key into a key container within a CSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
Opens an existing private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a792c39-71a7-4289-854d-98e6f749a526">Verify</a>
</td>
<td align="left" width="63%">
Verifies that a private key exists and can be used by the client but does not open the key.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509PrivateKey</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/40d2eae1-733a-4e5b-bb15-71301d73f438">Algorithm</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for the public key algorithm.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/035615f1-2dc7-47d7-98e4-7b5b0924030f">Certificate</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a byte array that contains the certificate associated with the private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1d56fa7e-8113-461d-a4f0-ebc048fbcb49">ContainerName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves the name of the key container.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/af5a30dd-4707-4b38-bf6b-b971d854d5b0">ContainerNamePrefix</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a prefix added to the name of the key container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/81cf4689-0cd6-4185-9242-ef26de9161a1">CspInformations</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a collection of <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> objects that contain information about the available cryptographic providers  that support the public key algorithm associated with the private key.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8bf6e62d-9ecf-4eee-9652-f04d2010b4f7">CspStatus</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves an <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object that contains information about the cryptographic provider and algorithm pair associated with the private key.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/31998dee-b656-47b8-acb5-246e1a10382a">DefaultContainer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the private key represents the default key container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a string that contains a description of the private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0ef32207-1fb0-49a2-95cf-353f907f3fc6">Existing</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that indicates whether the private key has been created or imported.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e3f04252-fe49-48fb-9e77-8a05031abf5f">ExportPolicy</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves export constraints for a private key.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93cd4fe0-5a08-4936-bbb0-6a723027e8c7">FriendlyName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a display name for the private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/39d8b9ac-ebbd-4bd8-8d5e-a4b28595b030">KeyProtection</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a  value that indicates how a private key is protected before use.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a value that identifies whether a private key can be used for signing, or encryption, or both.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e983c95b-6b3a-4e27-8a23-ef9051b11a16">KeyUsage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a  value that identifies the specific purpose for which a private key can be used.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/53a93aea-4435-4e04-9bd1-6356446aaefc">LegacyCsp</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies  or retrieves a Boolean value that indicates whether the provider is a CryptoAPI (legacy) cryptographic service provider (CSP).

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/de25aa05-bd65-49a6-9cd1-e18522c9e190">Length</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves the length, in bits, of the private key.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bdc3278e-3b5a-4ad0-9e9b-9639a2db4040">MachineContext</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that identifies the local certificate store context.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7f02b3d7-ab3a-4413-81ac-c626bc79a88c">Opened</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a Boolean value that specifies whether the private key is open.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/97243031-ef60-467d-ba65-6c7e6432d51f">ParentWindow</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves the ID of the window used to display key information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d81fad8a-767d-48c8-874a-c34843600b13">Pin</a>


</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
Specifies a personal identification number (PIN) that is used to authenticate users prior to accessing a private key container on a smart card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915743">ProviderName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves the name of the cryptographic provider.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5f4d2e29-8c02-4d9c-a3a6-15c222650c3e">ProviderType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves the type of cryptographic provider associated with the private key.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1c9bb81a-c91b-42b9-a44c-de1ae5b68af6">ReaderName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies the name of a smart card reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5fa1e5d8-b745-494c-a727-426084fce2a1">SecurityDescriptor</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> for the private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4f61a513-620c-48c4-b9dd-032b13a9f654">Silent</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that indicates whether the Certificate Enrollment Control is allowed to display  a dialog box when the private key is accessed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a1a6a474-5ffa-4b68-b84f-b0c9bea30ee5">UIContextMessage</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a string that contains user interface text associated with the private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93da413f-556d-4cda-8628-ce4a2150da19">UniqueContainerName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a unique name for the key container.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a>
 

 

