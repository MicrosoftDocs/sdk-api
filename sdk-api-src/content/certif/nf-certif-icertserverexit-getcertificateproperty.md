---
UID: NF:certif.ICertServerExit.GetCertificateProperty
title: ICertServerExit::GetCertificateProperty (certif.h)
description: Returns a named property from a certificate. (ICertServerExit.GetCertificateProperty)
helpviewer_keywords: ["CAType","CCertServerExit object [Security]","GetCertificateProperty method","CRLIndex","CRLState","CRLSuffix","CertCount","CertState","CertSuffix","GetCertificateProperty","GetCertificateProperty method [Security]","GetCertificateProperty method [Security]","CCertServerExit object","GetCertificateProperty method [Security]","ICertServerExit interface","ICertServerExit interface [Security]","GetCertificateProperty method","ICertServerExit.GetCertificateProperty","ICertServerExit::GetCertificateProperty","MachineDNSName","ModuleRegistryLocation","NotAfter","NotBefore","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","PublicKeyAlgorithm","RawCACertificate","RawCRL","RawCertificate","RawPublicKey","RawPublicKeyAlgorithmParameters","RequestID","RequesterCAAccess","SanitizedCAName","SanitizedShortName","SerialNumber","_certsrv_icertserverexit_getcertificateproperty","certif/ICertServerExit::GetCertificateProperty","fUseDS","security.icertserverexit_getcertificateproperty"]
old-location: security\icertserverexit_getcertificateproperty.htm
tech.root: security
ms.assetid: 7a6185cd-fae5-4ee6-b403-c7613b31e48a
ms.date: 12/05/2018
ms.keywords: CAType, CCertServerExit object [Security],GetCertificateProperty method, CRLIndex, CRLState, CRLSuffix, CertCount, CertState, CertSuffix, GetCertificateProperty, GetCertificateProperty method [Security], GetCertificateProperty method [Security],CCertServerExit object, GetCertificateProperty method [Security],ICertServerExit interface, ICertServerExit interface [Security],GetCertificateProperty method, ICertServerExit.GetCertificateProperty, ICertServerExit::GetCertificateProperty, MachineDNSName, ModuleRegistryLocation, NotAfter, NotBefore, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, PublicKeyAlgorithm, RawCACertificate, RawCRL, RawCertificate, RawPublicKey, RawPublicKeyAlgorithmParameters, RequestID, RequesterCAAccess, SanitizedCAName, SanitizedShortName, SerialNumber, _certsrv_icertserverexit_getcertificateproperty, certif/ICertServerExit::GetCertificateProperty, fUseDS, security.icertserverexit_getcertificateproperty
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
 - ICertServerExit::GetCertificateProperty
 - certif/ICertServerExit::GetCertificateProperty
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
 - ICertServerExit.GetCertificateProperty
 - CCertServerExit.GetCertificateProperty
---

# ICertServerExit::GetCertificateProperty


## -description

The <b>GetCertificateProperty</b> method returns a named property from a certificate.

## -parameters

### -param strPropertyName [in]

Specifies the named property to retrieve. There is a stock set of certificate properties, referred to as the <i>name properties</i>, that are always valid and can be retrieved by calling this method. For information about these properties, see 
<a href="/windows/desktop/SecCrypto/name-properties">Name Properties</a>. Other properties that can be retrieved include the certificate properties.
						

The following properties are unique to certificates and can be read by <b>GetCertificateProperty</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NotBefore"></a><a id="notbefore"></a><a id="NOTBEFORE"></a><dl>
<dt><b>NotBefore</b></dt>
<dt>Date/Time</dt>
</dl>
</td>
<td width="60%">
Certificate start validity date

</td>
</tr>
<tr>
<td width="40%"><a id="NotAfter"></a><a id="notafter"></a><a id="NOTAFTER"></a><dl>
<dt><b>NotAfter</b></dt>
<dt>Date/Time</dt>
</dl>
</td>
<td width="60%">
Certificate expiration date

</td>
</tr>
<tr>
<td width="40%"><a id="PublicKeyAlgorithm"></a><a id="publickeyalgorithm"></a><a id="PUBLICKEYALGORITHM"></a><dl>
<dt><b>PublicKeyAlgorithm</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
Subject key algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID)

</td>
</tr>
<tr>
<td width="40%"><a id="RawCertificate"></a><a id="rawcertificate"></a><a id="RAWCERTIFICATE"></a><dl>
<dt><b>RawCertificate</b></dt>
<dt>Binary</dt>
</dl>
</td>
<td width="60%">
Raw certificate bytes

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
<td width="40%"><a id="RequestID"></a><a id="requestid"></a><a id="REQUESTID"></a><dl>
<dt><b>RequestID</b></dt>
<dt>Signed Long</dt>
</dl>
</td>
<td width="60%">
Internal request ID

</td>
</tr>
<tr>
<td width="40%"><a id="SerialNumber"></a><a id="serialnumber"></a><a id="SERIALNUMBER"></a><dl>
<dt><b>SerialNumber</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
Certificate serial number

</td>
</tr>
</table>
 

The certificate's DistinguishedName, RawName, and SerialNumber properties are accessible by <b>GetCertificateProperty</b> only after the policy module has finished processing the request and the certificate is issued.

The following properties apply to the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>. The context must be  zero to read any of these properties. The context is set to zero when the <a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a> object is initially created.  It can also be set to zero by invoking the <a href="/windows/desktop/api/certif/nf-certif-icertserverexit-setcontext">SetContext</a> method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CAType"></a><a id="catype"></a><a id="CATYPE"></a><dl>
<dt><b>CAType</b></dt>
<dt>Long</dt>
</dl>
</td>
<td width="60%">
Type of <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>. This can be one of the following values (defined in Certsrv.h): 




ENUM_ENTERPRISE_ROOTCA

ENUM_ENTERPRISE_SUBCA

ENUM_STANDALONE_ROOTCA

ENUM_STANDALONE_SUBCA

</td>
</tr>
<tr>
<td width="40%"><a id="CertCount"></a><a id="certcount"></a><a id="CERTCOUNT"></a><dl>
<dt><b>CertCount</b></dt>
<dt>Long</dt>
</dl>
</td>
<td width="60%">
Number of CA certificates. This value will be one plus the number of times that the CA has been renewed. For information about renewal, see 
<a href="/windows/desktop/SecCrypto/certification-authority-renewal">Certification Authority Renewal</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CertState"></a><a id="certstate"></a><a id="CERTSTATE"></a><dl>
<dt><b>CertState</b></dt>
<dt>Long</dt>
</dl>
</td>
<td width="60%">
CA certificate <a href="/windows/desktop/SecGloss/s-gly">state</a>. This can be one of the following values:

<dl>
<dd>CA_DISP_ERROR: The CA certificate was never issued.</dd>
<dd>CA_DISP_REVOKED: The CA certificate has been revoked.</dd>
<dd>CA_DISP_VALID: The CA certificate is still valid.</dd>
<dd>CA_DISP_INVALID: The CA certificate has expired.</dd>
</dl>
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
Suffix for the CA certificate. The suffix is an empty string for CA certificates with an index of zero; otherwise, the suffix (in the form of "(<i>nn</i>)", where <i>nn</i> is the certificate index) is applied to all URLs that point to CA certificates stored in files or directory service objects. For non-<a href="/windows/desktop/SecGloss/l-gly">LDAP</a> URLs, the suffix typically appears before the ".crt" text. For LDAP URLs, the suffix is typically appended to the first 'CN=' in the full distinguished name.

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
<a href="/windows/desktop/SecGloss/c-gly">Certificate revocation list</a> (CRL) index. Appending a certificate index to this property name allows you to retrieve the CRL index. The CRL index does not necessarily match the certificate index. For more information, see 
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
CRL <a href="/windows/desktop/SecGloss/s-gly">state</a>. This can be one of the following values:

<dl>
<dd>CA_DISP_ERROR: The CRL is managed by another CA certificate.</dd>
<dd>CA_DISP_REVOKED: All unexpired CA certificates that use this CA certificate's CRL have been revoked.</dd>
<dd>CA_DISP_VALID: The CA certificate is still being used to publish CRLs as needed.</dd>
<dd>CA_DISP_INVALID: All CA certificates that use this CA certificate's CRL are expired.</dd>
</dl>
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
Suffix for the CA CRL. The suffix is an empty string for CRLs with an index of zero; otherwise, the suffix (in the form of "(<i>nn</i>)", where <i>nn</i> is the CRL index) is applied to all URLs pointing to CRLs stored in files or directory service objects. For non-LDAP URLs, the suffix typically appears before the ".crl" text. For LDAP URLs, the suffix typically is appended to the first 'CN=' in the full distinguished name.

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
DNS name of server hosting the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="ModuleRegistryLocation"></a><a id="moduleregistrylocation"></a><a id="MODULEREGISTRYLOCATION"></a><dl>
<dt><b>ModuleRegistryLocation</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
Registry location available for use by the module.

</td>
</tr>
<tr>
<td width="40%"><a id="RawCACertificate"></a><a id="rawcacertificate"></a><a id="RAWCACERTIFICATE"></a><dl>
<dt><b>RawCACertificate</b></dt>
<dt>Binary</dt>
</dl>
</td>
<td width="60%">
CA certificate.

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
CA's <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL).

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
<a href="/windows/desktop/SecGloss/s-gly">Sanitized name</a> for the CA. For information about sanitized CA names, see 
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
<a href="/windows/desktop/SecGloss/s-gly">Sanitized name</a> for the CA, shortened and containing a <a href="/windows/desktop/SecGloss/h-gly">hash</a> value to ensure uniqueness.

</td>
</tr>
</table>

### -param PropertyType [in]

Specifies the property type. The type can be one of the following.

<table>
<tr>
<th>Value</th>
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

A pointer to a <b>VARIANT</b> that will contain the property value. The returned value is encoded as a <b>BSTR</b>. Use the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysstringbytelen">SysStringByteLen</a> function to retrieve the length of the <b>BSTR</b>.  The binary <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> is stored as a <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a>  encoded X.509 certificate.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the requested property value.

## -remarks

You must call 
<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-setcontext">ICertServerExit::SetContext</a> prior to using this method.


#### Examples


```cpp
BSTR    bstrPropName = NULL;
VARIANT varProp;

VariantInit(&varProp);

// Set the property name to RequestID.
bstrPropName = SysAllocString(L"RequestID");

// Retrieve the certificate property.
// pCertServerExit has been used to call SetContext previously.
hr = pCertServerExit->GetCertificateProperty(bstrPropName,
                                             PROPTYPE_LONG,
                                             &varProp );
if (FAILED(hr))
{
    printf("Failed GetCertificateProperty [%x]\n", hr);
    goto error;
}
else
{
    // Successfully retrieved property; use varProp as needed.
    // ...
}

// Done processing.
if (NULL != bstrPropName)
    SysFreeString(bstrPropName);
VariantClear(&varProp);
```

## -see-also

<a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-setcontext">ICertServerExit::SetContext</a>



<a href="/windows/desktop/SecCrypto/name-properties">Name Properties</a>
