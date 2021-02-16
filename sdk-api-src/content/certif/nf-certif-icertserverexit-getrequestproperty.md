---
UID: NF:certif.ICertServerExit.GetRequestProperty
title: ICertServerExit::GetRequestProperty (certif.h)
description: Returns a named property from a request.
helpviewer_keywords: ["CCertServerExit object [Security]","GetRequestProperty method","CR_IN_KEYGEN","CR_IN_PKCS10","CR_IN_PKCS7","Disposition","DispositionMessage","GetRequestProperty","GetRequestProperty method [Security]","GetRequestProperty method [Security]","CCertServerExit object","GetRequestProperty method [Security]","ICertServerExit interface","ICertServerExit interface [Security]","GetRequestProperty method","ICertServerExit.GetRequestProperty","ICertServerExit::GetRequestProperty","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","RawCACertificate","RawRequest","RequestAttributes","RequestID","RequestType","RequesterName","ResolvedWhen","StatusCode","SubmittedWhen","_certsrv_icertserverexit_getrequestproperty","certif/ICertServerExit::GetRequestProperty","security.icertserverexit_getrequestproperty"]
old-location: security\icertserverexit_getrequestproperty.htm
tech.root: security
ms.assetid: e9b98573-4eb0-4add-988b-dc34d6c15436
ms.date: 12/05/2018
ms.keywords: CCertServerExit object [Security],GetRequestProperty method, CR_IN_KEYGEN, CR_IN_PKCS10, CR_IN_PKCS7, Disposition, DispositionMessage, GetRequestProperty, GetRequestProperty method [Security], GetRequestProperty method [Security],CCertServerExit object, GetRequestProperty method [Security],ICertServerExit interface, ICertServerExit interface [Security],GetRequestProperty method, ICertServerExit.GetRequestProperty, ICertServerExit::GetRequestProperty, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, RawCACertificate, RawRequest, RequestAttributes, RequestID, RequestType, RequesterName, ResolvedWhen, StatusCode, SubmittedWhen, _certsrv_icertserverexit_getrequestproperty, certif/ICertServerExit::GetRequestProperty, security.icertserverexit_getrequestproperty
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
 - ICertServerExit::GetRequestProperty
 - certif/ICertServerExit::GetRequestProperty
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
 - ICertServerExit.GetRequestProperty
 - CCertServerExit.GetRequestProperty
---

# ICertServerExit::GetRequestProperty


## -description

The <b>GetRequestProperty</b> method returns a named property from a request.

Note that the request is used to hold all associated states for the request and the eventual granted certificate that is not a part of the certificate. Thus, data such as revocation times and disposition data are kept in the request data object.

## -parameters

### -param strPropertyName [in]

Specifies the property to retrieve. There is a stock set of certificate properties, referred to as the name properties, that are always valid and can be retrieved by calling this method. For information about these properties, see 
<a href="/windows/desktop/SecCrypto/name-properties">Name Properties</a>.

Other properties valid for <a href="/windows/desktop/SecGloss/c-gly">certificate requests</a> include the request properties.

<div class="alert"><b>Note</b>  The request's <b>DistinguishedName</b> and <b>RawName</b> properties are accessible by <b>GetRequestProperty</b> only if the certificate is requested by using a PKCS #10 certificate request or another supported request format that contains encoded subject name information. Note that KeyGen requests do not contain encoded subject name information.</div>
<div> </div>

The following properties are unique to requests and can be accessed by using the <b>GetRequestProperty</b> method.



<table>
<tr>
<th>Request property</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Disposition"></a><a id="disposition"></a><a id="DISPOSITION"></a><dl>
<dt><b>Disposition</b></dt>
<dt>Signed long</dt>
</dl>
</td>
<td width="60%">
Current request disposition

</td>
</tr>
<tr>
<td width="40%"><a id="DispositionMessage"></a><a id="dispositionmessage"></a><a id="DISPOSITIONMESSAGE"></a><dl>
<dt><b>DispositionMessage</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
Informational disposition message

</td>
</tr>
<tr>
<td width="40%"><a id="RawCACertificate"></a><a id="rawcacertificate"></a><a id="RAWCACERTIFICATE"></a><dl>
<dt><b>RawCACertificate</b></dt>
<dt>Binary</dt>
</dl>
</td>
<td width="60%">
Certificate for the issuing <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>

</td>
</tr>
<tr>
<td width="40%"><a id="RawRequest"></a><a id="rawrequest"></a><a id="RAWREQUEST"></a><dl>
<dt><b>RawRequest</b></dt>
<dt>Binary</dt>
</dl>
</td>
<td width="60%">
Raw request bytes

</td>
</tr>
<tr>
<td width="40%"><a id="RequestAttributes"></a><a id="requestattributes"></a><a id="REQUESTATTRIBUTES"></a><dl>
<dt><b>RequestAttributes</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
Attribute string (can be truncated)

</td>
</tr>
<tr>
<td width="40%"><a id="RequesterName"></a><a id="requestername"></a><a id="REQUESTERNAME"></a><dl>
<dt><b>RequesterName</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
The name of the requester in the form "<i>DomainName</i>&#92;<i>UserID</i>"

</td>
</tr>
<tr>
<td width="40%"><a id="RequestID"></a><a id="requestid"></a><a id="REQUESTID"></a><dl>
<dt><b>RequestID</b></dt>
<dt>Signed long</dt>
</dl>
</td>
<td width="60%">
Internal requestID

</td>
</tr>
<tr>
<td width="40%"><a id="RequestType"></a><a id="requesttype"></a><a id="REQUESTTYPE"></a><dl>
<dt><b>RequestType</b></dt>
<dt>Signed long</dt>
</dl>
</td>
<td width="60%">
Indicates PKCS #10 or KeyGen request

</td>
</tr>
<tr>
<td width="40%"><a id="ResolvedWhen"></a><a id="resolvedwhen"></a><a id="RESOLVEDWHEN"></a><dl>
<dt><b>ResolvedWhen</b></dt>
<dt>Date/time</dt>
</dl>
</td>
<td width="60%">
When resolved

</td>
</tr>
<tr>
<td width="40%"><a id="StatusCode"></a><a id="statuscode"></a><a id="STATUSCODE"></a><dl>
<dt><b>StatusCode</b></dt>
<dt>Signed long</dt>
</dl>
</td>
<td width="60%">
Windows error for last operation

</td>
</tr>
<tr>
<td width="40%"><a id="SubmittedWhen"></a><a id="submittedwhen"></a><a id="SUBMITTEDWHEN"></a><dl>
<dt><b>SubmittedWhen</b></dt>
<dt>Date/time</dt>
</dl>
</td>
<td width="60%">
When arrived

</td>
</tr>
</table>
 


The <b>RequestType</b> property will be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_IN_PKCS7"></a><a id="cr_in_pkcs7"></a><dl>
<dt><b>CR_IN_PKCS7</b></dt>
</dl>
</td>
<td width="60%">
PKCS #7 renewal or registration request

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_PKCS10"></a><a id="cr_in_pkcs10"></a><dl>
<dt><b>CR_IN_PKCS10</b></dt>
</dl>
</td>
<td width="60%">
PKCS #10 request

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_KEYGEN"></a><a id="cr_in_keygen"></a><dl>
<dt><b>CR_IN_KEYGEN</b></dt>
</dl>
</td>
<td width="60%">
Keygen request (Netscape format)

</td>
</tr>
</table>
 

In addition, other properties may be set by a specific request type, request extensions, or by named attributes set in the header of a request.

### -param PropertyType [in]

Specifies the property type. The type can be one of the following types.

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
Unicode string data

</td>
</tr>
</table>

### -param pvarPropertyValue [out]

A pointer to the <b>VARIANT</b> that will contain the request property type.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and *<i>pvarPropertyValue</i> is set to the <b>VARIANT</b> that contains the request property value.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the request property value.

## -remarks

You must call 
<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-setcontext">ICertServerExit::SetContext</a> prior to using this method.


#### Examples


```cpp
BSTR      bstrPropName = NULL;
VARIANT   varProp;

VariantInit( &varProp );

bstrPropName = SysAllocString(L"RequestID");

// Retrieve the request property.
// pCertServerExit has been used to call SetContext previously.
hr = pCertServerExit->GetRequestProperty( bstrPropName,
                                          PROPTYPE_LONG,
                                          &varProp );
if (FAILED(hr))
{
    printf("Failed GetRequestProperty [%x]\n", hr);
    goto error;
}
else
{
    // Successfully retrieved property; use varProp as needed.
    // ...
}

// Done processing.
VariantClear( &varProp );
if ( NULL != bstrPropName )
    SysFreeString( bstrPropName );
```

## -see-also

<a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-setcontext">ICertServerExit::SetContext</a>



<a href="/windows/desktop/SecCrypto/name-properties">Name Properties</a>