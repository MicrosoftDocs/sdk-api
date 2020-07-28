---
UID: NN:xenroll.ICEnroll3
title: ICEnroll3 (xenroll.h)
description: One of several interfaces that represent the Certificate Enrollment Control.
helpviewer_keywords: ["ICEnroll3","ICEnroll3 interface [Security]","ICEnroll3 interface [Security]","described","_xen_icenroll3","security.icenroll3","xenroll/ICEnroll3"]
old-location: security\icenroll3.htm
tech.root: security
ms.assetid: 4caa7e75-0116-4891-8bf2-ede09a05a440
ms.date: 12/05/2018
ms.keywords: ICEnroll3, ICEnroll3 interface [Security], ICEnroll3 interface [Security],described, _xen_icenroll3, security.icenroll3, xenroll/ICEnroll3
f1_keywords:
- xenroll/ICEnroll3
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
- ICEnroll3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICEnroll3 interface


## -description


<p class="CCE_Message">[This interface is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ICEnroll3</b> interface is one of several interfaces that represent the Certificate Enrollment Control. It is primarily of interest if you are not using Automation. If, on the other hand, you are programming in Visual Basic or another Automation language, see the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICEnroll3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>, <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>, and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. <b>ICEnroll3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICEnroll3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptfilepkcs7">acceptFilePKCS7</a>
</td>
<td align="left" width="63%">
Accepts and processes a file that contains a PKCS #7 message containing a certificate.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptpkcs7">acceptPKCS7</a>
</td>
<td align="left" width="63%">
Accepts and processes a PKCS #7 message containing a certificate. The PKCS #7 is input as a parameter.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll2-addcerttypetorequest">addCertTypeToRequest</a>
</td>
<td align="left" width="63%">
Adds a certificate template to a request (used to support the enterprise <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> (CA)).</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll2-addnamevaluepairtosignature">addNameValuePairToSignature</a>
</td>
<td align="left" width="63%">
Adds the name and value pair of an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">attribute</a> to the request. It is up to the CA to interpret the meaning of the name-value pair.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-createfilepkcs10">createFilePKCS10</a>
</td>
<td align="left" width="63%">
Creates a base64-encoded PKCS #10 <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate request</a> and saves it in a file.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-createpkcs10">createPKCS10</a>
</td>
<td align="left" width="63%">
Creates a base64-encoded PKCS #10 certificate request.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-enumalgs">EnumAlgs</a>
</td>
<td align="left" width="63%">
Retrieves the IDs of cryptographic algorithms in a given algorithm class that are supported by the current CSP.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-enumcontainers">enumContainers</a>
</td>
<td align="left" width="63%">
Retrieves the names of the containers for the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providername">ProviderName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-enumproviders">enumProviders</a>
</td>
<td align="left" width="63%">
Retrieves the names of the available CSPs specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providertype">ProviderType</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-freerequestinfo">freeRequestInfo</a>
</td>
<td align="left" width="63%">
Cleans up the stores if an error occurs. Currently not implemented.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castoreflags">get_CAStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castoreflags">CAStoreFlags</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castorename">get_CAStoreName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castorename">CAStoreName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castoretype">get_CAStoreType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castoretype">CAStoreType</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_containername">get_ContainerName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_containername">ContainerName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_deleterequestcert">get_DeleteRequestCert</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_deleterequestcert">DeleteRequestCert</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_enablesmimecapabilities">get_EnableSMIMECapabilities</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_enablesmimecapabilities">EnableSMIMECapabilities</a> property.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll2-get_enablet61dnencoding">get_EnableT61DNEncoding</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll2-get_enablet61dnencoding">EnableT61DNEncoding</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_genkeyflags">get_GenKeyFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_genkeyflags">GenKeyFlags</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_hashalgid">get_HashAlgID</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_hashalgid">HashAlgID</a> property.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_hashalgorithm">get_HashAlgorithm</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_hashalgorithm">HashAlgorithm</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_keyspec">get_KeySpec</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_keyspec">KeySpec</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_limitexchangekeytoencipherment">get_LimitExchangeKeyToEncipherment</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_limitexchangekeytoencipherment">LimitExchangeKeyToEncipherment</a> property.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystoreflags">get_MyStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystoreflags">MyStoreFlags</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystorename">get_MyStoreName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystorename">MyStoreName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystoretype">get_MyStoreType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystoretype">MyStoreType</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providerflags">get_ProviderFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providerflags">ProviderFlags</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providername">get_ProviderName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providername">ProviderName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providertype">get_ProviderType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providertype">ProviderType</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_pvkfilename">get_PVKFileName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_pvkfilename">PVKFileName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststoreflags">get_RequestStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststoreflags">RequestStoreFlags</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststorename">get_RequestStoreName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststorename">RequestStoreName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststoretype">get_RequestStoreType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststoretype">RequestStoreType</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_reusehardwarekeyifunabletogennew">get_ReuseHardwareKeyIfUnableToGenNew</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_reusehardwarekeyifunabletogennew">ReuseHardwareKeyIfUnableToGenNew</a> property.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstoreflags">get_RootStoreFlags</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstoreflags">RootStoreFlags</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstorename">get_RootStoreName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstorename">RootStoreName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstoretype">get_RootStoreType</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstoretype">RootStoreType</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_spcfilename">get_SPCFileName</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_spcfilename">SPCFileName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_useexistingkeyset">get_UseExistingKeySet</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_useexistingkeyset">UseExistingKeySet</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_writecerttocsp">get_WriteCertToCSP</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_writecerttocsp">WriteCertToCSP</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll2-get_writecerttouserds">get_WriteCertToUserDS</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll2-get_writecerttouserds">WriteCertToUserDS</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-getalgname">GetAlgName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a cryptographic algorithm given its ID. The values retrieved by this method depend on the current CSP.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-getcertfrompkcs7">getCertFromPKCS7</a>
</td>
<td align="left" width="63%">
Retrieves the certificate, contained in a PKCS #7 message, that was  issued in response to a PKCS #10 certificate request.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-getkeylen">GetKeyLen</a>
</td>
<td align="left" width="63%">
Retrieves the minimum and maximum key lengths for the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">signature</a> and <a href="https://docs.microsoft.com/windows/desktop/SecGloss/e-gly">exchange keys</a>.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-getsupportedkeyspec">GetSupportedKeySpec</a>
</td>
<td align="left" width="63%">
Retrieves information regarding the CSP's support for signature or exchange keys.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-installpkcs7">InstallPKCS7</a>
</td>
<td align="left" width="63%">
Processes a certificate or chain of certificates, placing them into the appropriate <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate stores</a>. This method differs from the  <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptpkcs7">acceptPKCS7</a> method in that  <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-installpkcs7">InstallPKCS7</a> does not receive a request certificate.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystoreflags">put MyStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystoreflags">MyStoreFlags</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castoreflags">put_CAStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castoreflags">CAStoreFlags</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castorename">put_CAStoreName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castorename">CAStoreName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castoretype">put_CAStoreType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castoretype">CAStoreType</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_containername">put_ContainerName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_containername">ContainerName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_deleterequestcert">put_DeleteRequestCert</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_deleterequestcert">DeleteRequestCert</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_enablesmimecapabilities">put_EnableSMIMECapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_enablesmimecapabilities">EnableSMIMECapabilities</a> property.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll2-get_enablet61dnencoding">put_EnableT61DNEncoding</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll2-get_enablet61dnencoding">EnableT61DNEncoding</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_genkeyflags">put_GenKeyFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_genkeyflags">GenKeyFlags</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_hashalgid">put_HashAlgID</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_hashalgid">HashAlgID</a> property.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_hashalgorithm">put_HashAlgorithm</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_hashalgorithm">HashAlgorithm</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_keyspec">put_KeySpec</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_keyspec">KeySpec</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_limitexchangekeytoencipherment">put_LimitExchangeKeyToEncipherment</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_limitexchangekeytoencipherment">LimitExchangeKeyToEncipherment</a> property.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystorename">put_MyStoreName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystorename">MyStoreName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystoretype">put_MyStoreType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystoretype">MyStoreType</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providerflags">put_ProviderFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providerflags">ProviderFlags</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providername">put_ProviderName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providername">ProviderName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providertype">put_ProviderType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providertype">ProviderType</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_pvkfilename">put_PVKFileName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_pvkfilename">PVKFileName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststoreflags">put_RequestStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststoreflags">RequestStoreFlags</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststorename">put_RequestStoreName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststorename">RequestStoreName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststoretype">put_RequestStoreType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststoretype">RequestStoreType</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_reusehardwarekeyifunabletogennew">put_ReuseHardwareKeyIfUnableToGenNew</a>
</td>
<td align="left" width="63%">
Retrieves the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_reusehardwarekeyifunabletogennew">ReuseHardwareKeyIfUnableToGenNew</a> property.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstoreflags">put_RootStoreFlags</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstoreflags">RootStoreFlags</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstorename">put_RootStoreName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstorename">RootStoreName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstoretype">put_RootStoreType</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstoretype">RootStoreType</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_spcfilename">put_SPCFileName</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_spcfilename">SPCFileName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_useexistingkeyset">put_UseExistingKeySet</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_useexistingkeyset">UseExistingKeySet</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_writecerttocsp">put_WriteCertToCSP</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_writecerttocsp">WriteCertToCSP</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll2-get_writecerttouserds">put_WriteCertToUserDS</a>
</td>
<td align="left" width="63%">
Sets the value of the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll2-get_writecerttouserds">WriteCertToUserDS</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-reset">Reset</a>
</td>
<td align="left" width="63%">
 Returns the certificate enrollment control  object to its initial <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">state</a>.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICEnroll3</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castoreflags">CAStoreFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a flag that controls the certificate store when it is opened.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castorename">CAStoreName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the name of the store where all non-"ROOT" and non-"MY" certificates are kept.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castoretype">CAStoreType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the type of store to use for the store specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castorename">CAStoreName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_containername">ContainerName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the  name of the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">key container</a> to use.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_deleterequestcert">DeleteRequestCert</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean indicator that controls whether dummy certificates in the request store are deleted.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_enablesmimecapabilities">EnableSMIMECapabilities</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether the PKCS10 will contain a signed <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">attribute</a> for <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) capabilities.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll2-get_enablet61dnencoding">EnableT61DNEncoding</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether the distinguished name in the request is encoded as a T61 string instead of as a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/u-gly">UNICODE</a> string.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_genkeyflags">GenKeyFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a flag that controls whether a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">private key</a> is exportable.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_hashalgid">HashAlgID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the hash algorithm used when signing a PKCS #10 certificate request.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_hashalgorithm">HashAlgorithm</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves only the signature <a href="https://docs.microsoft.com/windows/desktop/SecGloss/h-gly">hash algorithm</a> used to sign the PKCS #10.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_keyspec">KeySpec</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the  type of key generated.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_limitexchangekeytoencipherment">LimitExchangeKeyToEncipherment</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether an AT_KEYEXCHANGE request contains <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">digital signature</a> and non-repudiation key usages.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystoreflags">MyStoreFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets the registry location used for the MY store.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystorename">MyStoreName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the name of the store  where certificates with linked private keys are kept.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystoretype">MyStoreType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the type of store  specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystorename">MyStoreName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providerflags">ProviderFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the CSP type.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providername">ProviderName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the name of the CSP to use.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providertype">ProviderType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the type of provider.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_pvkfilename">PVKFileName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the name of the file that will contain exported keys.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststoreflags">RequestStoreFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the registry location used for the REQUEST store.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststorename">RequestStoreName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the store that contains the dummy certificate. This dummy certificate, along with the added private keys, remains in the request store  until a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a> processes the request and responds with a PKCS #7.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststoretype">RequestStoreType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves the type of store to use for the store specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststorename">RequestStoreName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll3-get_reusehardwarekeyifunabletogennew">ReuseHardwareKeyIfUnableToGenNew</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that determines the action taken by the 
certificate enrollment control object if an error is encountered when generating a new key.</p> (Inherited from <b>ICEnroll3</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstoreflags">RootStoreFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the registry location used for the ROOT store.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstorename">RootStoreName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the root store where all intrinsically trusted self-signed <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">ROOT certificates</a> are kept.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstoretype">RootStoreType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the type of store to use for the store specified by the 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstorename">RootStoreName</a> property.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_spcfilename">SPCFileName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the file to write the resulting base64-encoded PKCS #7 (in <b>BSTR</b> form) as returned from the certification authority.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_useexistingkeyset">UseExistingKeySet</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Sets or retrieves a Boolean value that indicates whether the existing keys should be used.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_writecerttocsp">WriteCertToCSP</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that indicates whether a certificate should be written to the CSP.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-icenroll2-get_writecerttouserds">WriteCertToUserDS</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a Boolean value that controls whether the certificate is written to the user's Active Directory store.</p> (Inherited from <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

