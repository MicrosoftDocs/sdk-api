---
UID: NF:certcli.ICertRequest2.GetFullResponseProperty
title: ICertRequest2::GetFullResponseProperty (certcli.h)
description: Retrieves the cached response data returned by the server.
helpviewer_keywords: ["CCertRequest object [Security]","GetFullResponseProperty method","CR_OUT_BASE64","CR_OUT_BASE64HEADER","CR_OUT_BINARY","FR_PROP_ATTESTATIONCHALLENGE","FR_PROP_ATTESTATIONPROVIDERNAME","FR_PROP_BODYPARTSTRING","FR_PROP_CAEXCHANGECERTIFICATE","FR_PROP_CAEXCHANGECERTIFICATECHAIN","FR_PROP_CAEXCHANGECERTIFICATECRLCHAIN","FR_PROP_CAEXCHANGECERTIFICATEHASH","FR_PROP_ENCRYPTEDKEYHASH","FR_PROP_FAILINFO","FR_PROP_FULLRESPONSE","FR_PROP_FULLRESPONSENOPKCS7","FR_PROP_ISSUEDCERTIFICATE","FR_PROP_ISSUEDCERTIFICATECHAIN","FR_PROP_ISSUEDCERTIFICATECRLCHAIN","FR_PROP_ISSUEDCERTIFICATEHASH","FR_PROP_NONE","FR_PROP_OTHERINFOCHOICE","FR_PROP_PENDINFOTIME","FR_PROP_PENDINFOTOKEN","FR_PROP_STATUS","FR_PROP_STATUSINFOCOUNT","FR_PROP_STATUSSTRING","GetFullResponseProperty","GetFullResponseProperty method [Security]","GetFullResponseProperty method [Security]","CCertRequest object","GetFullResponseProperty method [Security]","ICertRequest interface","GetFullResponseProperty method [Security]","ICertRequest2 interface","GetFullResponseProperty method [Security]","ICertRequest3 interface","ICertRequest interface [Security]","GetFullResponseProperty method","ICertRequest2 interface [Security]","GetFullResponseProperty method","ICertRequest2.GetFullResponseProperty","ICertRequest2::GetFullResponseProperty","ICertRequest3 interface [Security]","GetFullResponseProperty method","ICertRequest3::GetFullResponseProperty","ICertRequest::GetFullResponseProperty","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","_certsrv_icertrequest2_getfullresponseproperty","certcli/ICertRequest2::GetFullResponseProperty","certcli/ICertRequest3::GetFullResponseProperty","certcli/ICertRequest::GetFullResponseProperty","security.icertrequest2_getfullresponseproperty"]
old-location: security\icertrequest2_getfullresponseproperty.htm
tech.root: security
ms.assetid: 1ee979b7-2d2a-4140-8eef-5e3a5e0c132c
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],GetFullResponseProperty method, CR_OUT_BASE64, CR_OUT_BASE64HEADER, CR_OUT_BINARY, FR_PROP_ATTESTATIONCHALLENGE, FR_PROP_ATTESTATIONPROVIDERNAME, FR_PROP_BODYPARTSTRING, FR_PROP_CAEXCHANGECERTIFICATE, FR_PROP_CAEXCHANGECERTIFICATECHAIN, FR_PROP_CAEXCHANGECERTIFICATECRLCHAIN, FR_PROP_CAEXCHANGECERTIFICATEHASH, FR_PROP_ENCRYPTEDKEYHASH, FR_PROP_FAILINFO, FR_PROP_FULLRESPONSE, FR_PROP_FULLRESPONSENOPKCS7, FR_PROP_ISSUEDCERTIFICATE, FR_PROP_ISSUEDCERTIFICATECHAIN, FR_PROP_ISSUEDCERTIFICATECRLCHAIN, FR_PROP_ISSUEDCERTIFICATEHASH, FR_PROP_NONE, FR_PROP_OTHERINFOCHOICE, FR_PROP_PENDINFOTIME, FR_PROP_PENDINFOTOKEN, FR_PROP_STATUS, FR_PROP_STATUSINFOCOUNT, FR_PROP_STATUSSTRING, GetFullResponseProperty, GetFullResponseProperty method [Security], GetFullResponseProperty method [Security],CCertRequest object, GetFullResponseProperty method [Security],ICertRequest interface, GetFullResponseProperty method [Security],ICertRequest2 interface, GetFullResponseProperty method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetFullResponseProperty method, ICertRequest2 interface [Security],GetFullResponseProperty method, ICertRequest2.GetFullResponseProperty, ICertRequest2::GetFullResponseProperty, ICertRequest3 interface [Security],GetFullResponseProperty method, ICertRequest3::GetFullResponseProperty, ICertRequest::GetFullResponseProperty, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, _certsrv_icertrequest2_getfullresponseproperty, certcli/ICertRequest2::GetFullResponseProperty, certcli/ICertRequest3::GetFullResponseProperty, certcli/ICertRequest::GetFullResponseProperty, security.icertrequest2_getfullresponseproperty
req.header: certcli.h
req.include-header: Certsrv.h
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
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertRequest2::GetFullResponseProperty
 - certcli/ICertRequest2::GetFullResponseProperty
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
 - ICertRequest3.GetFullResponseProperty
 - ICertRequest2.GetFullResponseProperty
 - ICertRequest.GetFullResponseProperty
 - CCertRequest.GetFullResponseProperty
---

# ICertRequest2::GetFullResponseProperty


## -description

The <b>GetFullResponseProperty</b> method retrieves the cached response data returned by the server.

## -parameters

### -param PropId [in]

The data to be retrieved. If the property is indexed, use <i>PropIndex</i> to specify the index.
               This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_NONE"></a><a id="fr_prop_none"></a><dl>
<dt><b>FR_PROP_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No data.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_FULLRESPONSE"></a><a id="fr_prop_fullresponse"></a><dl>
<dt><b>FR_PROP_FULLRESPONSE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
All the cached data is retrieved (binary data).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_STATUSINFOCOUNT"></a><a id="fr_prop_statusinfocount"></a><dl>
<dt><b>FR_PROP_STATUSINFOCOUNT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The number of responses in cache data (long, indexed property).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_BODYPARTSTRING"></a><a id="fr_prop_bodypartstring"></a><dl>
<dt><b>FR_PROP_BODYPARTSTRING</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Hierarchy data (string, indexed property).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_STATUS"></a><a id="fr_prop_status"></a><dl>
<dt><b>FR_PROP_STATUS</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The request status value (long, indexed property).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_STATUSSTRING"></a><a id="fr_prop_statusstring"></a><dl>
<dt><b>FR_PROP_STATUSSTRING</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The request status string (string, indexed property).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_OTHERINFOCHOICE"></a><a id="fr_prop_otherinfochoice"></a><dl>
<dt><b>FR_PROP_OTHERINFOCHOICE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Choice for other information (long, indexed property). This can be one of the following values.

<ul>
<li>CMC_OTHER_INFO_NO_CHOICE</li>
<li>CMC_OTHER_INFO_FAIL_CHOICE</li>
<li>CMC_OTHER_INFO_PEND_CHOICE</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_FAILINFO"></a><a id="fr_prop_failinfo"></a><dl>
<dt><b>FR_PROP_FAILINFO</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
The request failure information (long, indexed property).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_PENDINFOTOKEN"></a><a id="fr_prop_pendinfotoken"></a><dl>
<dt><b>FR_PROP_PENDINFOTOKEN</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The request pending token (binary, indexed property).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_PENDINFOTIME"></a><a id="fr_prop_pendinfotime"></a><dl>
<dt><b>FR_PROP_PENDINFOTIME</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
The request pending date (<b>DATE</b>, indexed property).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_ISSUEDCERTIFICATEHASH"></a><a id="fr_prop_issuedcertificatehash"></a><dl>
<dt><b>FR_PROP_ISSUEDCERTIFICATEHASH</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
The hash of the issued certificate is retrieved (binary, indexed property).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_ISSUEDCERTIFICATE"></a><a id="fr_prop_issuedcertificate"></a><dl>
<dt><b>FR_PROP_ISSUEDCERTIFICATE</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
The issued certificate is retrieved (binary, indexed property).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_ISSUEDCERTIFICATECHAIN"></a><a id="fr_prop_issuedcertificatechain"></a><dl>
<dt><b>FR_PROP_ISSUEDCERTIFICATECHAIN</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
The issued certificate (binary, indexed property).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_ISSUEDCERTIFICATECRLCHAIN"></a><a id="fr_prop_issuedcertificatecrlchain"></a><dl>
<dt><b>FR_PROP_ISSUEDCERTIFICATECRLCHAIN</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
The issued certificate chain (binary, indexed property).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_ENCRYPTEDKEYHASH"></a><a id="fr_prop_encryptedkeyhash"></a><dl>
<dt><b>FR_PROP_ENCRYPTEDKEYHASH</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
The encrypted key hash (binary, indexed property).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_FULLRESPONSENOPKCS7"></a><a id="fr_prop_fullresponsenopkcs7"></a><dl>
<dt><b>FR_PROP_FULLRESPONSENOPKCS7</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
All the cached data is retrieved except for the PKCS #7 (binary).

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_CAEXCHANGECERTIFICATEHASH"></a><a id="fr_prop_caexchangecertificatehash"></a><dl>
<dt><b>FR_PROP_CAEXCHANGECERTIFICATEHASH</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
The CA exchange certificate hash.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_CAEXCHANGECERTIFICATE"></a><a id="fr_prop_caexchangecertificate"></a><dl>
<dt><b>FR_PROP_CAEXCHANGECERTIFICATE</b></dt>
<dt>17</dt>
</dl>
</td>
<td width="60%">
The CA exchange certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_CAEXCHANGECERTIFICATECHAIN"></a><a id="fr_prop_caexchangecertificatechain"></a><dl>
<dt><b>FR_PROP_CAEXCHANGECERTIFICATECHAIN</b></dt>
<dt>18</dt>
</dl>
</td>
<td width="60%">
The CA exchange certificate chain.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_CAEXCHANGECERTIFICATECRLCHAIN"></a><a id="fr_prop_caexchangecertificatecrlchain"></a><dl>
<dt><b>FR_PROP_CAEXCHANGECERTIFICATECRLCHAIN</b></dt>
<dt>19</dt>
</dl>
</td>
<td width="60%">
The CA exchange certificate CLR chain.

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_ATTESTATIONCHALLENGE"></a><a id="fr_prop_attestationchallenge"></a><dl>
<dt><b>FR_PROP_ATTESTATIONCHALLENGE</b></dt>
<dt>20</dt>
</dl>
</td>
<td width="60%">
The key attestation challenge response

</td>
</tr>
<tr>
<td width="40%"><a id="FR_PROP_ATTESTATIONPROVIDERNAME"></a><a id="fr_prop_attestationprovidername"></a><dl>
<dt><b>FR_PROP_ATTESTATIONPROVIDERNAME</b></dt>
<dt>21</dt>
</dl>
</td>
<td width="60%">
The name of the key storage provider for key attestation.

</td>
</tr>
</table>

### -param PropIndex [in]

The zero-based index when <i>PropId</i> is an indexed property. If <i>PropId</i> is not an indexed property, then <i>PropIndex</i> must be zero.

### -param PropType [in]

The type of data returned in <i>pvarPropertyValue</i>. The property type here must match the type of data specified by the <i>PropId</i> parameter. 



This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_LONG"></a><a id="proptype_long"></a><dl>
<dt><b>PROPTYPE_LONG</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Signed long data.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_DATE"></a><a id="proptype_date"></a><dl>
<dt><b>PROPTYPE_DATE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Date data (includes date and time).

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_BINARY"></a><a id="proptype_binary"></a><dl>
<dt><b>PROPTYPE_BINARY</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Binary data.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_STRING"></a><a id="proptype_string"></a><dl>
<dt><b>PROPTYPE_STRING</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
String data.

</td>
</tr>
</table>

### -param Flags [in]

The format of the data returned in <i>pvarPropertyValue</i>. The flag set here must match the type of data specified by the <i>PropId</i> parameter. 



For more information, see Remarks.
               This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BASE64HEADER"></a><a id="cr_out_base64header"></a><dl>
<dt><b>CR_OUT_BASE64HEADER</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
BASE64 format with begin/end header.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BASE64"></a><a id="cr_out_base64"></a><dl>
<dt><b>CR_OUT_BASE64</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
BASE64 format without begin/end header.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BINARY"></a><a id="cr_out_binary"></a><dl>
<dt><b>CR_OUT_BINARY</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Binary format.

</td>
</tr>
</table>

### -param pvarPropertyValue [out]

The data returned.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK and  <i>pvarPropertyValue</i> contains the returned data.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>Variant</b> that contains the returned data.

## -remarks

The following <i>PropId</i> values return binary data, which means that the <i>Flags</i> parameter must set to CR_OUT_BINARY:

<ul>
<li>FR_PROP_FULLRESPONSE</li>
<li>FR_PROP_ISSUEDCERTIFICATEHASH</li>
<li>FR_PROP_ISSUEDCERTIFICATE</li>
<li>FR_PROP_ISSUEDCERTIFICATECHAIN</li>
<li>FR_PROP_ISSUEDCERTIFICATECRLCHAIN</li>
<li>FR_PROP_ENCRYPTEDKYEHASH</li>
<li>FR_PROP_FULLRESPONSENOPKCS7</li>
</ul>
This method is called after the <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-submit">ICertRequest3::Submit</a> or <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-retrievepending">ICertRequest3::RetrievePending</a> methods have been called. These methods populate the cached data that is returned by <b>GetFullResponseProperty</b>.

After the <b>ICertRequest3::GetFullResponseProperty</b> method returns its data, the following methods can be called:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll4-acceptresponse">ICEnroll4::AcceptResponse</a> can be called to install the returned certificate.</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll4-getcertfromresponse">ICEnroll4::GetCertFromResponse</a> can be called to parse the certificate from the response.</li>
</ul>