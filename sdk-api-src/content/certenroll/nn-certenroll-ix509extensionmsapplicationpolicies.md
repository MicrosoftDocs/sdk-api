---
UID: NN:certenroll.IX509ExtensionMSApplicationPolicies
title: IX509ExtensionMSApplicationPolicies
author: windows-sdk-content
description: Enables you to specify a collection of object identifiers (OIDs) that indicate how a certificate can be used by an application.
old-location: security\ix509extensionmsapplicationpolicies.htm
tech.root: seccertenroll
ms.assetid: 35b6449e-5a82-4f47-bdda-5356f44bb1fd
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509ExtensionMSApplicationPolicies, IX509ExtensionMSApplicationPolicies interface [Security], IX509ExtensionMSApplicationPolicies interface [Security],described, certenroll/IX509ExtensionMSApplicationPolicies, security.ix509extensionmsapplicationpolicies
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
 - IX509ExtensionMSApplicationPolicies
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionMSApplicationPolicies interface


## -description


The <b>IX509ExtensionMSApplicationPolicies</b> interface enables you to specify a collection of <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifiers</a> (OIDs) that indicate how a certificate can be used by an application. It is therefore similar to the <b>EnhancedKeyUsage</b> (EKU) extension. You can define your own OIDs or use any of the following EKU OIDs.<table>
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
<td>The certificate can be used to sign a request for automatic enrollment  in a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate trust list</a> (CTL).</td>
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
<td>The certificate can be used for archiving a <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a> on a  <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a>.</td>
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
 



A single policy is defined by an <a href="https://msdn.microsoft.com/en-us/library/Aa375225(v=VS.85).aspx">ICertificatePolicy</a> object. A collection is defined by an <a href="https://msdn.microsoft.com/en-us/library/Aa375214(v=VS.85).aspx">ICertificatePolicies</a> object. You can use the collection to initialize an <b>IX509ExtensionMSApplicationPolicies</b> object.

You can use this extension to specify which applications can use a certificate or force an application to accept only certificates for which certain OIDs have been listed. Typically, the application reviews the certificate to ensure that the <b>MSApplicationPolicies</b> extension contains the required OIDs.

To add this extension object to a  PKCS #10 request or a CMC request, you must first add it to an <a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a> collection and use the collection to initialize an <a href="https://msdn.microsoft.com/en-us/library/Aa377090(v=VS.85).aspx">IX509AttributeExtensions</a> object. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa379077(v=VS.85).aspx">PKCS #10 Extensions</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa374900(v=VS.85).aspx">CMC Extensions</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionMSApplicationPolicies</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>. <b>IX509ExtensionMSApplicationPolicies</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IX509ExtensionMSApplicationPolicies</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378160(v=VS.85).aspx">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the  extension from a <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa378161(v=VS.85).aspx">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the extension from an <a href="https://msdn.microsoft.com/en-us/library/Aa375214(v=VS.85).aspx">ICertificatePolicies</a> collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509ExtensionMSApplicationPolicies</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa378167(v=VS.85).aspx">Policies</a>


</td>
<td align="left" width="63%">
Retrieves a collection of application policies.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374874(v=VS.85).aspx">Certificate Enrollment API</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa382409(v=VS.85).aspx">Extensions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>
 

 

