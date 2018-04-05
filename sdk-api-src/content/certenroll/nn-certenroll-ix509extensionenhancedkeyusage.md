---
UID: NN:certenroll.IX509ExtensionEnhancedKeyUsage
title: IX509ExtensionEnhancedKeyUsage
author: windows-driver-content
description: Can be used to define a collection of object identifiers (OIDs) that identify the intended uses of the public key contained in the certificate.
old-location: security\ix509extensionenhancedkeyusage.htm
old-project: SecCertEnroll
ms.assetid: 0b9606d0-351c-4d2d-b876-545a9c2cf916
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IX509ExtensionEnhancedKeyUsage, IX509ExtensionEnhancedKeyUsage interface [Security], IX509ExtensionEnhancedKeyUsage interface [Security], described, certenroll/IX509ExtensionEnhancedKeyUsage, security.ix509extensionenhancedkeyusage
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509ExtensionEnhancedKeyUsage
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionEnhancedKeyUsage interface


## -description


The <b>IX509ExtensionEnhancedKeyUsage</b> interface can be used to define a collection of <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) that identify the intended uses of the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> contained in the certificate. The <b>EnhancedKeyUsage</b> extension can be used in addition to or in place of the <b>KeyUsage</b> extension. Also, the <b>EnhancedKeyUsage</b> extension and the <b>MSApplicationPolicies</b> extension defined by the <a href="https://msdn.microsoft.com/35b6449e-5a82-4f47-bdda-5356f44bb1fd">IX509ExtensionMSApplicationPolicies</a> interface are similar. The following syntax shows the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) structure  of the extension. The extension value is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) and included in the certificate request. 
<pre class="syntax" xml:space="preserve"><code>
----------------------------------------------------------------------
-- EnhancedKeyUsage
-- XCN_OID_ENHANCED_KEY_USAGE (2.5.29.37)
----------------------------------------------------------------------

EnhancedKeyUsage ::= SEQUENCE OF UsageIdentifier

UsageIdentifier ::= EncodedObjectID
</code></pre>You can define your own OIDs or use any of the following EKU OIDs. The list is not complete.<table>
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
<td>The certificate can be used to sign a request for automatic enrollment  in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL).</td>
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
<td>The certificate can be used for archiving a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> on a  <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>.</td>
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
<td>The certificate can be used to sign a certificate root list.</td>
</tr>
<tr>
<td>XCN_OID_WHQL_CRYPTO(1.3.6.1.4.1.311.10.3.5)

</td>
<td>The certificate can be used for Windows Hardware Quality Labs (WHQL) cryptography. </td>
</tr>
</table>
 



To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/d216bcfd-50be-4445-87a5-d1cb223aa70c">IX509AttributeExtensions</a> object. For more information, see <a href="https://msdn.microsoft.com/26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e">PKCS #10 Extensions</a> and <a href="https://msdn.microsoft.com/3aa9175b-f889-4d5d-8eb2-a8a42f9fe750">CMC Extensions</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionEnhancedKeyUsage</b> interface inherits from <a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>. <b>IX509ExtensionEnhancedKeyUsage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509ExtensionEnhancedKeyUsage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e83d0577-8eb9-4a59-8f52-ce1d9ab7f58a">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a DER-encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6cb12736-db5d-4d65-b32f-4bd11ceea01d">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension from a collection of <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> object identifiers that specify the intended uses of the public key.

[WebEnabled]

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionEnhancedKeyUsage</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/17a92139-0f6c-4371-b6cb-44185752abce">EnhancedKeyUsage</a>


</td>
<td align="left" width="63%">
Retrieves a collection of key usage OIDs.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ae6ab5fc-598e-43b8-a260-2cd94dc2648f">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>
 

 

