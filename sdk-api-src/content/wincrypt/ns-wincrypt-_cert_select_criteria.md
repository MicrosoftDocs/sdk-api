---
UID: NS:wincrypt._CERT_SELECT_CRITERIA
title: "_CERT_SELECT_CRITERIA"
author: windows-sdk-content
description: Specifies selection criteria that is passed to the CertSelectCertificateChains function.
old-location: security\cert_select_criteria.htm
tech.root: SecCrypto
ms.assetid: 246722a9-5db6-4a82-8f29-f60f0a2263e3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PCERT_SELECT_CRITERIA, CERT_SELECT_BY_ENHKEY_USAGE, CERT_SELECT_BY_EXTENSION, CERT_SELECT_BY_ISSUER_ATTR, CERT_SELECT_BY_ISSUER_NAME, CERT_SELECT_BY_KEY_USAGE, CERT_SELECT_BY_POLICY_OID, CERT_SELECT_BY_PROV_NAME, CERT_SELECT_BY_PUBLIC_KEY, CERT_SELECT_BY_SUBJECT_ATTR, CERT_SELECT_BY_SUBJECT_HOST_NAME, CERT_SELECT_BY_TLS_SIGNATURES, CERT_SELECT_CRITERIA, CERT_SELECT_CRITERIA structure [Security], PCCERT_SELECT_CRITERIA, PCCERT_SELECT_CRITERIA structure pointer [Security], PCERT_SELECT_CRITERIA, PCERT_SELECT_CRITERIA structure pointer [Security], _CERT_SELECT_CRITERIA, security.cert_select_criteria, wincrypt/CERT_SELECT_CRITERIA, wincrypt/PCCERT_SELECT_CRITERIA, wincrypt/PCERT_SELECT_CRITERIA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_SELECT_CRITERIA
product: Windows
targetos: Windows
req.typenames: CERT_SELECT_CRITERIA, *PCERT_SELECT_CRITERIA
req.redist: 
---

# _CERT_SELECT_CRITERIA structure


## -description


The <b>CERT_SELECT_CRITERIA</b> structure specifies selection criteria that is passed to the <a href="https://msdn.microsoft.com/b740772b-d25b-4b3d-9acb-03f7018750d6">CertSelectCertificateChains</a> function.


## -struct-fields




### -field dwType

Specifies the type of selection criteria used for the <b>ppPara</b> member. This member can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_BY_ENHKEY_USAGE"></a><a id="cert_select_by_enhkey_usage"></a><dl>
<dt><b>CERT_SELECT_BY_ENHKEY_USAGE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Select certificates  based on  a specific <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">enhanced key usage</a>. When this flag is set, the <i>ppPara</i> must reference a null-terminated <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) ANSI string that specifies the enhanced key usage.

This criteria is evaluated on the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_BY_KEY_USAGE"></a><a id="cert_select_by_key_usage"></a><dl>
<dt><b>CERT_SELECT_BY_KEY_USAGE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Select certificates  based on  a specific <b>szOID_KEY_USAGE</b> extension in the certificate.  When this flag is set, the <b>ppPara </b> member must reference a <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structure where the value of the extension is a <b>DWORD</b> that identifies the Key Usage bits.

This criteria is evaluated on the certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_BY_POLICY_OID"></a><a id="cert_select_by_policy_oid"></a><dl>
<dt><b>CERT_SELECT_BY_POLICY_OID</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Select certificates based on a specific issuance policy. The <b>ppPara</b> member must reference a null-terminated OID ANSI string of the desired issuance policy.

This criteria is evaluated on the issuance policy of the certificate chain.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_BY_PROV_NAME"></a><a id="cert_select_by_prov_name"></a><dl>
<dt><b>CERT_SELECT_BY_PROV_NAME</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Select certificates based on a specific <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> provider. The <b>ppPara</b> member must reference a  null-terminated Unicode string that represents the name of the provider.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_BY_EXTENSION"></a><a id="cert_select_by_extension"></a><dl>
<dt><b>CERT_SELECT_BY_EXTENSION</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Select certificates based on the presence of a specified extension and an optional specified value. The <b>ppPara</b> member must reference a <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structure that specifies the extension OID and the  associated value.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_BY_SUBJECT_HOST_NAME"></a><a id="cert_select_by_subject_host_name"></a><dl>
<dt><b>CERT_SELECT_BY_SUBJECT_HOST_NAME</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Select certificates based on the Subject DNS HOST Name. The <b>ppPara</b> member must reference a null-terminated Unicode string that contains the subject host name. The selection performed based on this flag  is the same as the evaluation of the <b>pwszServerName</b> member of the <a href="https://msdn.microsoft.com/3422693a-3fad-4ed8-9fab-d9a185476123">SSL_EXTRA_CERT_CHAIN_POLICY_PARA</a> structure during a call to the <a href="https://msdn.microsoft.com/19c37f77-1072-4740-b244-764b816a2a1f">CertVerifyCertificateChainPolicy</a> function. 

This criteria is evaluated on the certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_BY_ISSUER_ATTR"></a><a id="cert_select_by_issuer_attr"></a><dl>
<dt><b>CERT_SELECT_BY_ISSUER_ATTR</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Select certificates based on the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">relative distinguished name</a> (RDN) element of the issuer of the certificate.  The <b>ppPara</b> member must reference a <a href="https://msdn.microsoft.com/e84254b9-e9a7-4689-a12f-2772282c5433">CERT_RDN</a> structure that contains the RDN element of the issuer.

This criteria is evaluated on the certificate chain.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_BY_SUBJECT_ATTR"></a><a id="cert_select_by_subject_attr"></a><dl>
<dt><b>CERT_SELECT_BY_SUBJECT_ATTR</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Select certificates based on the RDN element in the Subject of the certificate.  The <b>ppPara</b> member must be a reference to a <a href="https://msdn.microsoft.com/e84254b9-e9a7-4689-a12f-2772282c5433">CERT_RDN</a> structure that contains the RDN element of the Subject.

This criteria is evaluated on the certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_BY_ISSUER_NAME"></a><a id="cert_select_by_issuer_name"></a><dl>
<dt><b>CERT_SELECT_BY_ISSUER_NAME</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Select certificates based on the issuer of the certificate. The <b>ppPara</b> member must be a reference to a <a href="https://msdn.microsoft.com/1c2a07b8-f702-47f3-8d4c-6ac0cbc63f0f">CERT_NAME_BLOB</a> structure that contains the name of the issuer.

This criteria is evaluated on the certificate chain.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_BY_PUBLIC_KEY"></a><a id="cert_select_by_public_key"></a><dl>
<dt><b>CERT_SELECT_BY_PUBLIC_KEY</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Select certificates based on the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> of the certificate.  The <b>ppPara</b> member must reference a pointer to  a <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure that contains the public key.

This criteria is evaluated on the certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SELECT_BY_TLS_SIGNATURES"></a><a id="cert_select_by_tls_signatures"></a><dl>
<dt><b>CERT_SELECT_BY_TLS_SIGNATURES</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Select certificates based on the <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">Transport Layer Security protocol</a> (TLS) Signature requirement. The <b>ppPara</b> member must reference a <a href="https://msdn.microsoft.com/b4b58175-1367-4c91-8680-523a4b125c76">SecPkgContext_SupportedSignatures</a> structure.

This criteria is evaluated on the certificate.

</td>
</tr>
</table>
 


### -field cPara

A <b>DWORD</b> value that specifies the number of search attributes specified in the <b>ppPara</b> member. 


### -field ppPara

A pointer to a pointer to one or more selection values.  The data type depends on the selection type specified by the <b>dwType</b> member. If more than one selection value is present, an application must match only one value.

