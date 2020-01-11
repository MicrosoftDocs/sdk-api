---
UID: NN:certenroll.IX509PrivateKey
title: IX509PrivateKey (certenroll.h)
description: Represents an asymmetric private key that can be used for encryption, signing, and key agreement.
old-location: security\ix509privatekey.htm
tech.root: seccertenroll
ms.assetid: 72612ea4-ed45-46ac-9dad-614a9a754d83
ms.date: 12/05/2018
ms.keywords: IX509PrivateKey, IX509PrivateKey interface [Security], IX509PrivateKey interface [Security],described, certenroll/IX509PrivateKey, security.ix509privatekey
f1_keywords:
- certenroll/IX509PrivateKey
dev_langs:
- c++
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CertEnroll.dll
api_name:
- IX509PrivateKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509PrivateKey interface


## -description


The <b>IX509PrivateKey</b> interface represents an asymmetric private key that can be used for encryption, signing, and key agreement.  Private keys are referenced in the following objects:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertykeyprovinfo">ICertPropertyKeyProvInfo</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributearchivekey">IX509AttributeArchiveKey</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509PrivateKey</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509PrivateKey</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-close">Close</a>
</td>
<td align="left" width="63%">
Releases the handle of the cryptographic service provider (CSP) or the handle of the Cryptography API: Next Generation (CNG) key storage provider (KSP).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-create">Create</a>
</td>
<td align="left" width="63%">
Creates an asymmetric  private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-delete">Delete</a>
</td>
<td align="left" width="63%">
Releases the handle of the CSP or KSP and deletes the key from disk or smart card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-export">Export</a>
</td>
<td align="left" width="63%">
Copies the private key to a byte array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-exportpublickey">ExportPublicKey</a>
</td>
<td align="left" width="63%">
Exports the public key portion of the asymmetric key pair.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-import">Import</a>
</td>
<td align="left" width="63%">
Imports an existing private key into a key container within a CSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-open">Open</a>
</td>
<td align="left" width="63%">
Opens an existing private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-verify">Verify</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_algorithm">Algorithm</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for the public key algorithm.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_certificate">Certificate</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_containername">ContainerName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_containernameprefix">ContainerNamePrefix</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_cspinformations">CspInformations</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves a collection of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> objects that contain information about the available cryptographic providers  that support the public key algorithm associated with the private key.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_cspstatus">CspStatus</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object that contains information about the cryptographic provider and algorithm pair associated with the private key.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_defaultcontainer">DefaultContainer</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_description">Description</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_existing">Existing</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_exportpolicy">ExportPolicy</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_friendlyname">FriendlyName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyprotection">KeyProtection</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyspec">KeySpec</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_keyusage">KeyUsage</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_legacycsp">LegacyCsp</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_length">Length</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_machinecontext">MachineContext</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_opened">Opened</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_parentwindow">ParentWindow</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-put_pin">Pin</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_providername">ProviderName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_providertype">ProviderType</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_readername">ReaderName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_securitydescriptor">SecurityDescriptor</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Specifies or retrieves the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security descriptor</a> for the private key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_silent">Silent</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_uicontextmessage">UIContextMessage</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509privatekey-get_uniquecontainername">UniqueContainerName</a>


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




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a>
 

 

