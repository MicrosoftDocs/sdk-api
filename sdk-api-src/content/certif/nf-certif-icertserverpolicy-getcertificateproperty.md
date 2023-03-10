---
UID: NF:certif.ICertServerPolicy.GetCertificateProperty
title: ICertServerPolicy::GetCertificateProperty (certif.h)
description: Returns a named property from a certificate. (ICertServerPolicy.GetCertificateProperty)
helpviewer_keywords: ["CAType","CCertServerPolicy object [Security]","GetCertificateProperty method","CRLIndex","CRLState","CRLSuffix","CertCount","CertState","CertSuffix","GeneralFlags","GetCertificateProperty","GetCertificateProperty method [Security]","GetCertificateProperty method [Security]","CCertServerPolicy object","GetCertificateProperty method [Security]","ICertServerPolicy interface","ICertServerPolicy interface [Security]","GetCertificateProperty method","ICertServerPolicy.GetCertificateProperty","ICertServerPolicy::GetCertificateProperty","MachineDNSName","ModuleRegistryLocation","NotAfter","NotBefore","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","PublicKeyAlgorithm","RawCACertificate","RawCRL","RawPublicKey","RawPublicKeyAlgorithmParameters","RequestID","RequesterCAAccess","RequesterNameFromOldCertificate","SanitizedCAName","SanitizedShortName","_certsrv_icertserverpolicy_getcertificateproperty","certif/ICertServerPolicy::GetCertificateProperty","fUseDS","security.icertserverpolicy_getcertificateproperty"]
old-location: security\icertserverpolicy_getcertificateproperty.htm
tech.root: security
ms.assetid: e7ece535-31c7-4468-a9ef-84f4dbf16d76
ms.date: 12/05/2018
ms.keywords: CAType, CCertServerPolicy object [Security],GetCertificateProperty method, CRLIndex, CRLState, CRLSuffix, CertCount, CertState, CertSuffix, GeneralFlags, GetCertificateProperty, GetCertificateProperty method [Security], GetCertificateProperty method [Security],CCertServerPolicy object, GetCertificateProperty method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],GetCertificateProperty method, ICertServerPolicy.GetCertificateProperty, ICertServerPolicy::GetCertificateProperty, MachineDNSName, ModuleRegistryLocation, NotAfter, NotBefore, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, PublicKeyAlgorithm, RawCACertificate, RawCRL, RawPublicKey, RawPublicKeyAlgorithmParameters, RequestID, RequesterCAAccess, RequesterNameFromOldCertificate, SanitizedCAName, SanitizedShortName, _certsrv_icertserverpolicy_getcertificateproperty, certif/ICertServerPolicy::GetCertificateProperty, fUseDS, security.icertserverpolicy_getcertificateproperty
req.header: certif.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertServerPolicy::GetCertificateProperty
 - certif/ICertServerPolicy::GetCertificateProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertServerPolicy.GetCertificateProperty
 - CCertServerPolicy.GetCertificateProperty
---

# ICertServerPolicy::GetCertificateProperty


## -description

The <b>GetCertificateProperty</b> method returns a named property from a certificate.

You must call 
<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">ICertServerPolicy::SetContext</a> prior to using this method.

## -parameters

### -param strPropertyName [in]

Specifies the named property to retrieve. There is a stock set of certificate properties, referred to as the <i>name properties</i>, that are always valid and can be retrieved by calling this method. For information about these properties, see 
<a href="/windows/desktop/SecCrypto/name-properties">Name Properties</a>. Other properties beside name properties can also be retrieved.

The certificate's DistinguishedName and RawName properties are accessible by <a href="/windows/desktop/api/certif/nf-certif-icertserverexit-getcertificateproperty">ICertServerExit::GetCertificateProperty</a> only after the policy module has finished processing the request and the certificate is issued. The issued certificate's DistinguishedName and RawName properties can also be read by an exit module by using <b>ICertServerExit::GetCertificateProperty</b>.

There are additional certificate properties that cannot be accessed by <b>GetCertificateProperty</b>. These properties are not set until after the policy module returns VR_INSTANT_OK and the certificate is issued. For a complete list of all the properties in an issued certificate, see 
<b>GetCertificateProperty</b>.


The following properties are unique to certificates and can be read by <b>GetCertificateProperty</b>.



<table>
<tr>
<th>Certificate property</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RequestID"></a><a id="requestid"></a><a id="REQUESTID"></a><dl>
<dt><b>RequestID</b></dt>
<dt>Signed long</dt>
</dl>
</td>
<td width="60%">
Internal request ID

</td>
</tr>
<tr>
<td width="40%"><a id="NotBefore"></a><a id="notbefore"></a><a id="NOTBEFORE"></a><dl>
<dt><b>NotBefore</b></dt>
<dt>Date/time</dt>
</dl>
</td>
<td width="60%">
Certificate start validity date

</td>
</tr>
<tr>
<td width="40%"><a id="NotAfter"></a><a id="notafter"></a><a id="NOTAFTER"></a><dl>
<dt><b>NotAfter</b></dt>
<dt>Date/time</dt>
</dl>
</td>
<td width="60%">
Certificate expiration date

</td>
</tr>
<tr>
<td width="40%"><a id="RawPublicKey"></a><a id="rawpublickey"></a><a id="RAWPUBLICKEY"></a><dl>
<dt><b>RawPublicKey</b></dt>
<dt>Binary</dt>
</dl>
</td>
<td width="60%">
Subject key

</td>
</tr>
<tr>
<td width="40%"><a id="PublicKeyAlgorithm"></a><a id="publickeyalgorithm"></a><a id="PUBLICKEYALGORITHM"></a><dl>
<dt><b>PublicKeyAlgorithm</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
Subject key algorithm <a href="/windows/desktop/SecGloss/o-gly">object ID</a> (OID)

</td>
</tr>
<tr>
<td width="40%"><a id="RawPublicKeyAlgorithmParameters"></a><a id="rawpublickeyalgorithmparameters"></a><a id="RAWPUBLICKEYALGORITHMPARAMETERS"></a><dl>
<dt><b>RawPublicKeyAlgorithmParameters</b></dt>
<dt>Binary</dt>
</dl>
</td>
<td width="60%">
Subject key algorithm parameters

</td>
</tr>
<tr>
<td width="40%"><a id="GeneralFlags"></a><a id="generalflags"></a><a id="GENERALFLAGS"></a><dl>
<dt><b>GeneralFlags</b></dt>
<dt>PROPTYPE_LONG</dt>
</dl>
</td>
<td width="60%">
GeneralFlags in the enrollment request. This is a bitwise <b>OR</b> of values. The only value of interest 								should be the flag value of 0x00000400, which tells the CA not to persist the request in the 									database. If  the CA is in databaseless mode (that is, for Windows Server 2008 R2 and later CAs, the CA's database 								has the 	<b>DBFLAGS_ENABLEVOLATILEREQUESTS</b> flag set), use <code>certutil -getreg DbFlags</code> and 									<code>certutil -setreg DBFlags</code> for configuring the CA in databaseless mode.


<b>Windows Vista and Windows Storage Server 2003:  </b>This field is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="RequesterNameFromOldCertificate"></a><a id="requesternamefromoldcertificate"></a><a id="REQUESTERNAMEFROMOLDCERTIFICATE"></a><dl>
<dt><b>RequesterNameFromOldCertificate</b></dt>
<dt>PROPTYPE_STRING</dt>
</dl>
</td>
<td width="60%">
For renewal requests, returns the requester account name (for example,  contoso\requester).

</td>
</tr>
</table>
 


The following properties apply to the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>.



<table>
<tr>
<th>CA property</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CAType"></a><a id="catype"></a><a id="CATYPE"></a><dl>
<dt><b>CAType</b></dt>
<dt>Long</dt>
</dl>
</td>
<td width="60%">
The type of certification authority. This can be one of the following values (defined in Certsrv.h):

<ul>
<li>ENUM_ENTERPRISE_ROOTCA</li>
<li>ENUM_ENTERPRISE_SUBCA</li>
<li>ENUM_STANDALONE_ROOTCA</li>
<li>ENUM_STANDALONE_SUBCA</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="CertCount"></a><a id="certcount"></a><a id="CERTCOUNT"></a><dl>
<dt><b>CertCount</b></dt>
<dt>Long</dt>
</dl>
</td>
<td width="60%">
The number of CA certificates. This value will be one plus the number of times that the CA has been renewed. For information about renewal, see 
<a href="/windows/desktop/SecCrypto/certification-authority-renewal">Certification</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CertState"></a><a id="certstate"></a><a id="CERTSTATE"></a><dl>
<dt><b>CertState</b></dt>
<dt>Long</dt>
</dl>
</td>
<td width="60%">
The CA certificate <a href="/windows/desktop/SecGloss/s-gly">state</a>. This can be one of the following values:

<ul>
<li>CA_DISP_ERROR: The CA certificate was never issued.</li>
<li>CA_DISP_REVOKED: The CA certificate has been revoked.</li>
<li>CA_DISP_VALID: The CA certificate is still valid.</li>
<li>CA_DISP_INVALID: The CA certificate has expired.</li>
</ul>
This property name may be appended with '.#', where # represents a CA certificate index (or, in the case of the CRLSuffix property, a CRL index). For information about certificate and CRL indices, see 
<a href="/windows/desktop/SecCrypto/certification-authority-renewal">Certification Authority Renewal</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CertSuffix"></a><a id="certsuffix"></a><a id="CERTSUFFIX"></a><dl>
<dt><b>CertSuffix</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
The suffix for the CA certificate. The suffix is an empty string for CA certificates with an index of zero; otherwise, the suffix (in the form of "(<i>nn</i>)", where <i>nn</i> is the certificate index) is applied to all URLs that point to CA certificates stored in files or directory service objects. For non-<a href="/windows/desktop/SecGloss/l-gly">LDAP</a> URLs, the suffix typically appears before the ".crt" text. For LDAP URLs, the suffix is typically appended to the first 'CN=' in the full distinguished name.

This property name may be appended with '.#', where # represents a CA certificate index (or, in the case of the CRLSuffix property, a CRL index). For information about certificate and CRL indices, see 
<a href="/windows/desktop/SecCrypto/certification-authority-renewal">Certification Authority Renewal</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRLIndex"></a><a id="crlindex"></a><a id="CRLINDEX"></a><dl>
<dt><b>CRLIndex</b></dt>
<dt>Long</dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) index. Appending a certificate index to this property name allows you to retrieve the CRL index. The CRL index does not necessarily match the certificate index. For more information, see 
<a href="/windows/desktop/SecCrypto/certification-authority-renewal">Certification</a>.

This property name may be appended with '.#', where # represents a CA certificate index (or, in the case of the CRLSuffix property, a CRL index). For information about certificate and CRL indices, see 
<a href="/windows/desktop/SecCrypto/certification-authority-renewal">Certification Authority Renewal</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRLState"></a><a id="crlstate"></a><a id="CRLSTATE"></a><dl>
<dt><b>CRLState</b></dt>
<dt>Long</dt>
</dl>
</td>
<td width="60%">
The CRL <a href="/windows/desktop/SecGloss/s-gly">state</a>. This can be one of the following values:

<ul>
<li>CA_DISP_ERROR: The CRL is managed by another CA certificate.</li>
<li>CA_DISP_REVOKED: All unexpired CA certificates using this CA certificate's CRL have been revoked.</li>
<li>CA_DISP_VALID: The CA certificate is still being used to publish CRLs as needed.</li>
<li>CA_DISP_INVALID: All CA certificates using this CA certificate's CRL are expired.</li>
</ul>
This property name may be appended with '.#', where # represents a CA certificate index (or, in the case of the CRLSuffix property, a CRL index). For information about certificate and CRL indices, see 
<a href="/windows/desktop/SecCrypto/certification-authority-renewal">Certification Authority Renewal</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRLSuffix"></a><a id="crlsuffix"></a><a id="CRLSUFFIX"></a><dl>
<dt><b>CRLSuffix</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
The suffix for the CA CRL. The suffix is an empty string for CRLs with an index of zero; otherwise, the suffix (in the form of "(<i>nn</i>)", where <i>nn</i> is the CRL index) is applied to all URLs that point to CRLs stored in files or directory service objects. For non-LDAP URLs, the suffix typically appears before the .crl text. For LDAP URLs, the suffix typically is appended to the first 'CN=' in the full distinguished name.

This property name may be appended with '.#', where # represents a CA certificate index (or, in the case of the CRLSuffix property, a CRL index). For information about certificate and CRL indices, see 
<a href="/windows/desktop/SecCrypto/certification-authority-renewal">Certification Authority Renewal</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="fUseDS"></a><a id="fuseds"></a><a id="FUSEDS"></a><dl>
<dt><b>fUseDS</b></dt>
<dt>Long</dt>
</dl>
</td>
<td width="60%">
Indicates whether the CA uses a directory service. This can be either of the following values:

<ul>
<li>0=no</li>
<li>1=yes</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="MachineDNSName"></a><a id="machinednsname"></a><a id="MACHINEDNSNAME"></a><dl>
<dt><b>MachineDNSName</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
The DNS name of the server hosting the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="ModuleRegistryLocation"></a><a id="moduleregistrylocation"></a><a id="MODULEREGISTRYLOCATION"></a><dl>
<dt><b>ModuleRegistryLocation</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
The registry location available for use by the module.

</td>
</tr>
<tr>
<td width="40%"><a id="RawCACertificate"></a><a id="rawcacertificate"></a><a id="RAWCACERTIFICATE"></a><dl>
<dt><b>RawCACertificate</b></dt>
<dt>Binary</dt>
</dl>
</td>
<td width="60%">
The CA certificate.

This property name may be appended with '.#', where # represents a CA certificate index (or, in the case of the CRLSuffix property, a CRL index). For information about certificate and CRL indices, see 
<a href="/windows/desktop/SecCrypto/certification-authority-renewal">Certification Authority Renewal</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="RawCRL"></a><a id="rawcrl"></a><a id="RAWCRL"></a><dl>
<dt><b>RawCRL</b></dt>
<dt>Binary</dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) of the CA.

This property name may be appended with '.#', where # represents a CA certificate index (or, in the case of the CRLSuffix property, a CRL index). For information about certificate and CRL indices, see 
<a href="/windows/desktop/SecCrypto/certification-authority-renewal">Certification Authority Renewal</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="RequesterCAAccess"></a><a id="requestercaaccess"></a><a id="REQUESTERCAACCESS"></a><dl>
<dt><b>RequesterCAAccess</b></dt>
<dt>Long</dt>
</dl>
</td>
<td width="60%">
Indicates whether the requester is authorized to request the certificate. This can be either of the following values:

<ul>
<li>0=no</li>
<li>1=yes</li>
</ul>
(The Certification Authority MMC snap-in can be used to control <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> permissions.)

</td>
</tr>
<tr>
<td width="40%"><a id="SanitizedCAName"></a><a id="sanitizedcaname"></a><a id="SANITIZEDCANAME"></a><dl>
<dt><b>SanitizedCAName</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/s-gly">sanitized name</a> for the CA. For information about sanitized CA names, see 
<a href="/windows/desktop/api/certcli/nf-certcli-icertconfig-getconfig">ICertConfig::GetConfig</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SanitizedShortName"></a><a id="sanitizedshortname"></a><a id="SANITIZEDSHORTNAME"></a><dl>
<dt><b>SanitizedShortName</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
The sanitized name for the CA, which is shortened and which contains a hash value to ensure uniqueness.

</td>
</tr>
</table>

### -param PropertyType [in]

Specifies the property type. The type can be one of the following values.

<table>
<tr>
<th>Type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_LONG"></a><a id="proptype_long"></a><dl>
<dt><b>PROPTYPE_LONG</b></dt>
</dl>
</td>
<td width="60%">
Signed long data

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_DATE"></a><a id="proptype_date"></a><dl>
<dt><b>PROPTYPE_DATE</b></dt>
</dl>
</td>
<td width="60%">
Date/time

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_BINARY"></a><a id="proptype_binary"></a><dl>
<dt><b>PROPTYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary data

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_STRING"></a><a id="proptype_string"></a><dl>
<dt><b>PROPTYPE_STRING</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/u-gly">Unicode</a> string data

</td>
</tr>
</table>

### -param pvarPropertyValue [out]

A pointer to <b>VARIANT</b> that will contain the property value.

## -returns

 If the method succeeds, the method returns S_OK, and *<i>pvarPropertyValue</i> is set to the <b>VARIANT</b> that contains the requested property value.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">ICertServerPolicy::SetContext</a>



<a href="/windows/desktop/SecCrypto/name-properties">Name Properties</a>
