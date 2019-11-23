---
UID: NN:xenroll.IEnroll2
title: IEnroll2 (xenroll.h)

description: Represents the Certificate Enrollment Control and is used primarily to generate certificate requests.
old-location: security\ienroll2.htm
tech.root: SecCrypto
ms.assetid: 60a28944-35de-4ea2-8523-5634685ac224

ms.date: 12/05/2018
ms.keywords: IEnroll2, IEnroll2 interface [Security], IEnroll2 interface [Security],described, security.ienroll2, xenroll/IEnroll2
ms.topic: interface
f1_keywords: 
 - "xenroll/IEnroll2"
dev_langs:
 - c++
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnroll2 interface


## -description


<p class="CCE_Message">[This interface is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>IEnroll2</b> interface represents the Certificate Enrollment Control and is used primarily to generate <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate requests</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnroll2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a>. <b>IEnroll2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IEnroll2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr">acceptFilePKCS7WStr</a>
</td>
<td align="left" width="63%">
Accepts and processes a PKCS #7 message containing a certificate, then stores the message to a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob">acceptPKCS7Blob</a>
</td>
<td align="left" width="63%">
Accepts and processes a PKCS #7 message containing a certificate. The PKCS #7 is input as a parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-addauthenticatedattributestopkcs7request">AddAuthenticatedAttributesToPKCS7Request</a>
</td>
<td align="left" width="63%">
Adds authenticated attributes to a PKCS #7 certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-addcerttypetorequestwstr">AddCertTypeToRequestWStr</a>
</td>
<td align="left" width="63%">
Adds a certificate template to a request (used to support the enterprise <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> (CA)).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-addextensionstorequest">AddExtensionsToRequest</a>
</td>
<td align="left" width="63%">
Adds extensions to the certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-addnamevaluepairtosignaturewstr">AddNameValuePairToSignatureWStr</a>
</td>
<td align="left" width="63%">
Adds the name and value pair of an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">attribute</a> to the request. It is up to the CA to interpret the meaning of the name-value pair.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-createfilepkcs10wstr">createFilePKCS10WStr</a>
</td>
<td align="left" width="63%">
Creates a base64-encoded PKCS #10 <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate request</a> and saves it in a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs10wstr">createPKCS10WStr</a>
</td>
<td align="left" width="63%">
Creates a base64-encoded PKCS #10 certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-createpkcs7requestfromrequest">CreatePKCS7RequestFromRequest</a>
</td>
<td align="left" width="63%">
Creates a PKCS #7 request from an existing certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-enumalgs">EnumAlgs</a>
</td>
<td align="left" width="63%">
Retrieves the IDs of cryptographic algorithms in a given algorithm class that are supported by the current CSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumcontainerswstr">enumContainersWStr</a>
</td>
<td align="left" width="63%">
Retrieves the names of the containers for the CSP specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr">ProviderNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumproviderswstr">enumProvidersWStr</a>
</td>
<td align="left" width="63%">
Retrieves the names of the available <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service providers</a> (CSPs) specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype">ProviderType</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-freerequestinfoblob">freeRequestInfoBlob</a>
</td>
<td align="left" width="63%">
Deletes a certificate context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags">get_CAStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags">CAStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr">get_CAStoreNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr">CAStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr">get_CAStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr">CAStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr">get_ContainerNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr">ContainerNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert">get_DeleteRequestCert</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert">DeleteRequestCert</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities">get_EnableSMIMECapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities">EnableSMIMECapabilities</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_enablet61dnencoding">get_EnableT61DNEncoding</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_enablet61dnencoding">EnableT61DNEncoding</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags">get_GenKeyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags">GenKeyFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid">get_HashAlgID</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid">HashAlgID</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr">get_HashAlgorithmWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr">HashAlgorithmWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec">get_KeySpec</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec">KeySpec</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment">get_LimitExchangeKeyToEncipherment</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment">LimitExchangeKeyToEncipherment</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags">get_MyStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags">MyStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr">get_MyStoreNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr">MyStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr">get_MyStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr">MyStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags">get_ProviderFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags">ProviderFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr">get_ProviderNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr">ProviderNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype">get_ProviderType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype">ProviderType</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr">get_PVKFileNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr">PVKFileNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate">get_RenewalCertificate</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate">RenewalCertificate</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags">get_RequestStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags">RequestStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr">get_RequestStoreNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr">RequestStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr">get_RequestStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr">RequestStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew">get_ReuseHardwareKeyIfUnableToGenNew</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew">ReuseHardwareKeyIfUnableToGenNew</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags">get_RootStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags">RootStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr">get_RootStoreNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr">RootStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr">get_RootStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr">RootStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr">get_SPCFileNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr">SPCFileNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset">get_UseExistingKeySet</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset">UseExistingKeySet</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp">get_WriteCertToCSP</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp">WriteCertToCSP</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds">get_WriteCertToUserDS</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds">WriteCertToUserDS</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getalgnamewstr">GetAlgNameWStr</a>
</td>
<td align="left" width="63%">
Retrieves the name of a cryptographic algorithm given its ID. The values retrieved by this method depend on the current CSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-getcastore">getCAStore</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-getcertcontextfrompkcs7">getCertContextFromPKCS7</a>
</td>
<td align="left" width="63%">
Retrieves the certificate, contained in a PKCS #7 message, that was  issued in response to a PKCS #10 certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getkeylen">GetKeyLen</a>
</td>
<td align="left" width="63%">
Retrieves the minimum and maximum key lengths for the signature and exchange keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-getmystore">getMyStore</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-getroothstore">getROOTHStore</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getsupportedkeyspec">GetSupportedKeySpec</a>
</td>
<td align="left" width="63%">
Retrieves information regarding the CSP's support for signature or exchange keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-installpkcs7blob">InstallPKCS7Blob</a>
</td>
<td align="left" width="63%">
Processes a certificate or chain of certificates, placing them into the appropriate <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate stores</a>. This method differs from the  <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob">acceptPKCS7Blob</a> method in that  <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-installpkcs7blob">InstallPKCS7Blob</a> does not receive a request certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags">put_CAStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags">CAStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr">put_CAStoreNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr">CAStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr">put_CAStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr">CAStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr">put_ContainerNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr">ContainerNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert">put_DeleteRequestCert</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert">DeleteRequestCert</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities">put_EnableSMIMECapabilities</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities">EnableSMIMECapabilities</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_enablet61dnencoding">put_EnableT61DNEncoding</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_enablet61dnencoding">EnableT61DNEncoding</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags">put_GenKeyFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags">GenKeyFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid">put_HashAlgID</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid">HashAlgID</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr">put_HashAlgorithmWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr">HashAlgorithmWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec">put_KeySpec</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec">KeySpec</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment">put_LimitExchangeKeyToEncipherment</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment">LimitExchangeKeyToEncipherment</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags">put_MyStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags">MyStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr">put_MyStoreNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr">MyStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr">put_MyStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr">MyStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags">put_ProviderFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags">ProviderFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr">put_ProviderNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr">ProviderNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype">put_ProviderType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype">ProviderType</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr">put_PVKFileNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr">PVKFileNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate">put_RenewalCertificate</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate">RenewalCertificate</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags">put_RequestStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags">RequestStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr">put_RequestStoreNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr">RequestStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr">put_RequestStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr">RequestStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew">put_ReuseHardwareKeyIfUnableToGenNew</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew">ReuseHardwareKeyIfUnableToGenNew</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags">put_RootStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags">RootStoreFlags</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr">put_RootStoreNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr">RootStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr">put_RootStoreTypeWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr">RootStoreTypeWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr">put_SPCFileNameWStr</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr">SPCFileNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset">put_UseExistingKeySet</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset">UseExistingKeySet</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp">put_WriteCertToCSP</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp">WriteCertToCSP</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds">put_WriteCertToUserDS</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds">WriteCertToUserDS</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-reset">Reset</a>
</td>
<td align="left" width="63%">
 Returns the certificate enrollment control  object to its initial <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">state</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreca">SetHStoreCA</a>
</td>
<td align="left" width="63%">
Specifies the handle to use for the CA store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoremy">SetHStoreMy</a>
</td>
<td align="left" width="63%">
Specifies the handle to use for the MY store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstorerequest">SetHStoreRequest</a>
</td>
<td align="left" width="63%">
Specifies the handle to use for the request store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreroot">SetHStoreROOT</a>
</td>
<td align="left" width="63%">
Specifies the handle to use for the ROOT store.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnroll2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags">CAStoreFlags</a>


</td>
<td align="left" width="63%">
Sets or retrieves a flag that controls the certificate store when it is 
opened.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr">CAStoreNameWStr</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the name of the store where all non-"ROOT" and non-"MY" certificates are kept.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr">CAStoreTypeWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the type of store to use for the store specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr">CAStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr">ContainerNameWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the  name of the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">key container</a> to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_deleterequestcert">DeleteRequestCert</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean indicator that controls whether dummy certificates in the request store are deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_enablesmimecapabilities">EnableSMIMECapabilities</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether the PKCS #10 will contain a signed attribute for <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_enablet61dnencoding">EnableT61DNEncoding</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether the distinguished name in the request is encoded as a T61 string instead of as a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/u-gly">UNICODE</a> string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags">GenKeyFlags</a>


</td>
<td align="left" width="63%">
Sets or retrieves the values passed to <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a> when the certificate request is generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid">HashAlgID</a>


</td>
<td align="left" width="63%">
Sets or retrieves the hash algorithm used when signing a PKCS #10 certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr">HashAlgorithmWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves only the signature hash algorithm used to sign the PKCS #10.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec">KeySpec</a>


</td>
<td align="left" width="63%">
Sets or retrieves the  type of key generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment">LimitExchangeKeyToEncipherment</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether an AT_KEYEXCHANGE request contains <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">digital signature</a> and non-repudiation key usages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags">MyStoreFlags</a>


</td>
<td align="left" width="63%">
Sets or retrieves the registry location used for the MY store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr">MyStoreNameWStr</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the name of the store  where certificates with linked private keys are kept.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr">MyStoreTypeWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the type of store  specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr">MyStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags">ProviderFlags</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the CSP type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr">ProviderNameWStr</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the name of the CSP to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype">ProviderType</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the type of provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr">PVKFileNameWStr</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the name of the file that will contain exported keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_renewalcertificate">RenewalCertificate</a>


</td>
<td align="left" width="63%">
Specifies the certificate context for the renewal certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags">RequestStoreFlags</a>


</td>
<td align="left" width="63%">
Sets or retrieves the registry location used for the REQUEST store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr">RequestStoreNameWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the name of the store that contains the dummy certificate. This dummy certificate, along with the added private keys, remains in the request store  until a certification authority processes the request and responds with a PKCS #7.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr">RequestStoreTypeWStr</a>


</td>
<td align="left" width="63%">
 Sets or retrieves the type of store to use for the store specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr">RequestStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew">ReuseHardwareKeyIfUnableToGenNew</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that determines the action taken by the 
certificate enrollment control object if an error is encountered when generating a new key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags">RootStoreFlags</a>


</td>
<td align="left" width="63%">
Sets or retrieves the registry location used for the ROOT store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr">RootStoreNameWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the name of the root store where all intrinsically trusted self-signed ROOT certificates are kept.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr">RootStoreTypeWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the type of store to use for the store specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr">RootStoreNameWStr</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr">SPCFileNameWStr</a>


</td>
<td align="left" width="63%">
Sets or retrieves the name of the file to write the resulting base64-encoded PKCS #7 as returned from the certification authority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset">UseExistingKeySet</a>


</td>
<td align="left" width="63%">
 Sets or retrieves a Boolean value that indicates whether the existing keys should be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp">WriteCertToCSP</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that indicates whether a certificate should be written to the CSP.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds">WriteCertToUserDS</a>


</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether the certificate is written to the user's Active Directory store.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a>
 

 

