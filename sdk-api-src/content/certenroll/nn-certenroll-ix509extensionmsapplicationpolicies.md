---
UID: NN:certenroll.IX509ExtensionMSApplicationPolicies
title: IX509ExtensionMSApplicationPolicies (certenroll.h)
description: Enables you to specify a collection of object identifiers (OIDs) that indicate how a certificate can be used by an application.
helpviewer_keywords: ["IX509ExtensionMSApplicationPolicies","IX509ExtensionMSApplicationPolicies interface [Security]","IX509ExtensionMSApplicationPolicies interface [Security]","described","certenroll/IX509ExtensionMSApplicationPolicies","security.ix509extensionmsapplicationpolicies"]
old-location: security\ix509extensionmsapplicationpolicies.htm
tech.root: security
ms.assetid: 35b6449e-5a82-4f47-bdda-5356f44bb1fd
ms.date: 12/05/2018
ms.keywords: IX509ExtensionMSApplicationPolicies, IX509ExtensionMSApplicationPolicies interface [Security], IX509ExtensionMSApplicationPolicies interface [Security],described, certenroll/IX509ExtensionMSApplicationPolicies, security.ix509extensionmsapplicationpolicies
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509ExtensionMSApplicationPolicies
 - certenroll/IX509ExtensionMSApplicationPolicies
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509ExtensionMSApplicationPolicies
---

# IX509ExtensionMSApplicationPolicies interface


## -description

The <b>IX509ExtensionMSApplicationPolicies</b> interface enables you to specify a collection of <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) that indicate how a certificate can be used by an application. It is therefore similar to the <b>EnhancedKeyUsage</b> (EKU) extension. You can define your own OIDs or use any of the following EKU OIDs.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_OID_ANY_APPLICATION_POLICY(1.3.6.1.4.1.311.10.12.1)

</td>
<td>The applications that can use the certificate are not restricted.</td>
</tr>
<tr>
<td>XCN_OID_AUTO_ENROLL_CTL_USAGE(1.3.6.1.4.1.311.20.1)

</td>
<td>The certificate can be used to sign a request for automatic enrollment  in a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL).</td>
</tr>
<tr>
<td>XCN_OID_DRM(1.3.6.1.4.1.311.10.5.1)

</td>
<td>The certificate can be used for digital rights management applications.</td>
</tr>
<tr>
<td>XCN_OID_DS_EMAIL_REPLICATION(1.3.6.1.4.1.311.21.19)

</td>
<td>The certificate can be used for Directory Service email replication.</td>
</tr>
<tr>
<td>XCN_OID_EFS_RECOVERY(1.3.6.1.4.1.311.10.3.4.1)

</td>
<td>The certificate can be used for recovery  of documents protected by using Encrypting File System (EFS).</td>
</tr>
<tr>
<td>XCN_OID_EMBEDDED_NT_CRYPTO(1.3.6.1.4.1.311.10.3.8)

</td>
<td>The certificate can be used for Windows NT Embedded cryptography.</td>
</tr>
<tr>
<td>XCN_OID_ENROLLMENT_AGENT(1.3.6.1.4.1.311.20.2.1)

</td>
<td>The certificate can be used by an enrollment agent.</td>
</tr>
<tr>
<td>XCN_OID_IPSEC_KP_IKE_INTERMEDIATE(1.3.6.1.5.5.8.2.2)

</td>
<td>The certificate can be used for Internet Key Exchange (IKE).</td>
</tr>
<tr>
<td>XCN_OID_KP_CA_EXCHANGE(1.3.6.1.4.1.311.21.5)

</td>
<td>The certificate can be used for archiving a <a href="/windows/desktop/SecGloss/p-gly">private key</a> on a  <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>.</td>
</tr>
<tr>
<td>XCN_OID_KP_CTL_USAGE_SIGNING(1.3.6.1.4.1.311.10.3.1)

</td>
<td>The certificate can be used to sign a CTL.</td>
</tr>
<tr>
<td>XCN_OID_KP_DOCUMENT_SIGNING(1.3.6.1.4.1.311.10.3.12)

</td>
<td>The certificate can be used for signing documents.</td>
</tr>
<tr>
<td>XCN_OID_KP_EFS(1.3.6.1.4.1.311.10.3.4)

</td>
<td>The certificate can be used to encrypt files by using the Encrypting File System.</td>
</tr>
<tr>
<td>XCN_OID_KP_KEY_RECOVERY(1.3.6.1.4.1.311.10.3.11)

</td>
<td>The certificate can be used to encrypt and recover escrowed keys.</td>
</tr>
<tr>
<td>XCN_OID_KP_KEY_RECOVERY_AGENT(1.3.6.1.4.1.311.21.6)

</td>
<td>The certificate is  used to identify a key recovery agent.</td>
</tr>
<tr>
<td>XCN_OID_KP_LIFETIME_SIGNING(1.3.6.1.4.1.311.10.3.13)

</td>
<td>Limits the validity period of a signature to the validity period of the certificate. This restriction is typically used with the XCN_OID_PKIX_KP_CODE_SIGNING OID value to indicate that new time stamp semantics should be used.</td>
</tr>
<tr>
<td>XCN_OID_KP_QUALIFIED_SUBORDINATION(1.3.6.1.4.1.311.10.3.10)

</td>
<td>The certificate can be used to sign cross certificate and subordinate certification authority certificate requests. Qualified subordination is implemented by applying basic constraints, certificate policies, and application policies. Cross certification typically requires policy mapping.</td>
</tr>
<tr>
<td>XCN_OID_KP_SMARTCARD_LOGON(1.3.6.1.4.1.311.20.2.2)

</td>
<td>The certificate enables an individual to log on to a computer by using a smart card.</td>
</tr>
<tr>
<td>XCN_OID_KP_TIME_STAMP_SIGNING(1.3.6.1.4.1.311.10.3.2)

</td>
<td>The certificate can be used to sign a time stamp to be added to a document. Time stamp signing is typically part of a time stamping service.</td>
</tr>
<tr>
<td>XCN_OID_LICENSE_SERVER(1.3.6.1.4.1.311.10.6.2)

</td>
<td>The certificate can be used by a license server when transacting with Microsoft to receive licenses for Terminal Services clients.</td>
</tr>
<tr>
<td>XCN_OID_LICENSES(1.3.6.1.4.1.311.10.6.1)

</td>
<td>The certificate can be used for key pack licenses.</td>
</tr>
<tr>
<td>XCN_OID_NT5_CRYPTO(1.3.6.1.4.1.311.10.3.7)

</td>
<td>The certificate can be used for Windows Server 2003, Windows XP, and Windows 2000 cryptography.</td>
</tr>
<tr>
<td>XCN_OID_OEM_WHQL_CRYPTO(1.3.6.1.4.1.311.10.3.7)

</td>
<td>The certificate can be used for used for Original Equipment Manufacturers (OEM) Windows Hardware Quality Labs (WHQL) cryptography. 
</td>
</tr>
<tr>
<td>XCN_OID_PKIX_KP_CLIENT_AUTH(1.3.6.1.5.5.7.3.2)

</td>
<td>The certificate can be used for authenticating a client.</td>
</tr>
<tr>
<td>XCN_OID_PKIX_KP_CODE_SIGNING(1.3.6.1.5.5.7.3.3)

</td>
<td>The certificate can be used for signing code.</td>
</tr>
<tr>
<td>XCN_OID_PKIX_KP_EMAIL_PROTECTION(1.3.6.1.5.5.7.3.4)

</td>
<td>The certificate can be used to encrypt email messages.</td>
</tr>
<tr>
<td>XCN_OID_PKIX_KP_IPSEC_END_SYSTEM(1.3.6.1.5.5.7.3.5)

</td>
<td>The certificate can be used for signing  end-to-end Internet Protocol Security (IPSEC) communication.</td>
</tr>
<tr>
<td>XCN_OID_PKIX_KP_IPSEC_TUNNEL(1.3.6.1.5.5.7.3.6)

</td>
<td>The certificate can be used for singing IPSEC communication in tunnel mode.</td>
</tr>
<tr>
<td>XCN_OID_PKIX_KP_IPSEC_USER(1.3.6.1.5.5.7.3.7)

</td>
<td>The certificate can be used for an IPSEC user.</td>
</tr>
<tr>
<td>XCN_OID_PKIX_KP_OCSP_SIGNING(1.3.6.1.5.5.7.3.9)

</td>
<td>The certificate can be used for Online Certificate Status Protocol (OCSP) signing.</td>
</tr>
<tr>
<td>XCN_OID_PKIX_KP_SERVER_AUTH(1.3.6.1.5.5.7.3.1)

</td>
<td>The certificate can be used for OCSP authentication.</td>
</tr>
<tr>
<td>XCN_OID_PKIX_KP_TIMESTAMP_SIGNING(1.3.6.1.5.5.7.3.8)

</td>
<td>The certificate can be used for signing public key infrastructure timestamps.</td>
</tr>
<tr>
<td>XCN_OID_ROOT_LIST_SIGNER(1.3.6.1.4.1.311.10.3.9)

</td>
<td>The certificate can be used sign a certificate root list.</td>
</tr>
<tr>
<td>XCN_OID_WHQL_CRYPTO(1.3.6.1.4.1.311.10.3.5)

</td>
<td>The certificate can be used for Windows Hardware Quality Labs (WHQL) cryptography. </td>
</tr>
</table>
 



A single policy is defined by an <a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a> object. A collection is defined by an <a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicies">ICertificatePolicies</a> object. You can use the collection to initialize an <b>IX509ExtensionMSApplicationPolicies</b> object.

You can use this extension to specify which applications can use a certificate or force an application to accept only certificates for which certain OIDs have been listed. Typically, the application reviews the certificate to ensure that the <b>MSApplicationPolicies</b> extension contains the required OIDs.

To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a> collection and use the collection to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a> object. For more information, see <a href="/windows/desktop/SecCertEnroll/pkcs--10-extensions">PKCS #10 Extensions</a> and <a href="/windows/desktop/SecCertEnroll/cmc-extensions">CMC Extensions</a>.

## -inheritance

The <b>IX509ExtensionMSApplicationPolicies</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>. <b>IX509ExtensionMSApplicationPolicies</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="/windows/win32/seccrypto/extensions">Extensions</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
