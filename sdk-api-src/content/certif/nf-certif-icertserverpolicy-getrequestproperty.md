---
UID: NF:certif.ICertServerPolicy.GetRequestProperty
title: ICertServerPolicy::GetRequestProperty (certif.h)
description: Retrieves a specific property from a request.
helpviewer_keywords: ["CCertServerPolicy object [Security]","GetRequestProperty method","GetRequestProperty","GetRequestProperty method [Security]","GetRequestProperty method [Security]","CCertServerPolicy object","GetRequestProperty method [Security]","ICertServerPolicy interface","ICertServerPolicy interface [Security]","GetRequestProperty method","ICertServerPolicy.GetRequestProperty","ICertServerPolicy::GetRequestProperty","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","RawRequest","RequestAttributes","RequestID","RequestType","RequesterName","SubmittedWhen","_certsrv_icertserverpolicy_getrequestproperty","certif/ICertServerPolicy::GetRequestProperty","security.icertserverpolicy_getrequestproperty"]
old-location: security\icertserverpolicy_getrequestproperty.htm
tech.root: security
ms.assetid: 4055008a-7034-47f3-bbae-c870165ab3ef
ms.date: 12/05/2018
ms.keywords: CCertServerPolicy object [Security],GetRequestProperty method, GetRequestProperty, GetRequestProperty method [Security], GetRequestProperty method [Security],CCertServerPolicy object, GetRequestProperty method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],GetRequestProperty method, ICertServerPolicy.GetRequestProperty, ICertServerPolicy::GetRequestProperty, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, RawRequest, RequestAttributes, RequestID, RequestType, RequesterName, SubmittedWhen, _certsrv_icertserverpolicy_getrequestproperty, certif/ICertServerPolicy::GetRequestProperty, security.icertserverpolicy_getrequestproperty
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
 - ICertServerPolicy::GetRequestProperty
 - certif/ICertServerPolicy::GetRequestProperty
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
 - ICertServerPolicy.GetRequestProperty
 - CCertServerPolicy.GetRequestProperty
---

# ICertServerPolicy::GetRequestProperty


## -description

The <b>GetRequestProperty</b> method retrieves a specific property from a request.

## -parameters

### -param strPropertyName [in]

Specifies the name of the property to retrieve. This parameter can be set to a name property or  a request property.

Name properties include  a stock set of certificate properties that are always valid and can be retrieved by calling this method. For information about these properties, see 
<a href="/windows/desktop/SecCrypto/name-properties">Name Properties</a>.

Request properties are unique to requests and include the following possible values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RequestID"></a><a id="requestid"></a><a id="REQUESTID"></a><dl>
<dt><b>RequestID</b></dt>
<dt>Signed long</dt>
</dl>
</td>
<td width="60%">
Internal requestID.

</td>
</tr>
<tr>
<td width="40%"><a id="RawRequest"></a><a id="rawrequest"></a><a id="RAWREQUEST"></a><dl>
<dt><b>RawRequest</b></dt>
<dt>Binary</dt>
</dl>
</td>
<td width="60%">
Raw request bytes.

</td>
</tr>
<tr>
<td width="40%"><a id="RequestAttributes"></a><a id="requestattributes"></a><a id="REQUESTATTRIBUTES"></a><dl>
<dt><b>RequestAttributes</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
Attribute string (may be truncated).

</td>
</tr>
<tr>
<td width="40%"><a id="RequestType"></a><a id="requesttype"></a><a id="REQUESTTYPE"></a><dl>
<dt><b>RequestType</b></dt>
<dt>Signed long</dt>
</dl>
</td>
<td width="60%">
Indicates PKCS #10 or KeyGen request. For more information about this property, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="SubmittedWhen"></a><a id="submittedwhen"></a><a id="SUBMITTEDWHEN"></a><dl>
<dt><b>SubmittedWhen</b></dt>
<dt>Date/time</dt>
</dl>
</td>
<td width="60%">
When arrived.

</td>
</tr>
<tr>
<td width="40%"><a id="RequesterName"></a><a id="requestername"></a><a id="REQUESTERNAME"></a><dl>
<dt><b>RequesterName</b></dt>
<dt>String</dt>
</dl>
</td>
<td width="60%">
The name of the requester in the form "<i>DomainName</i>&#92;<i>UserID</i>".

</td>
</tr>
</table>
 

<b>Note</b>  There are additional request properties that cannot be accessed by <b>GetRequestProperty</b> because they  are not set until after the policy module finishes processing the request.In addition, other properties may be set by a specific request type, request extensions, or by named attributes set in the header of a request.

### -param PropertyType [in]

Specifies the property type. The <i>PropertyType</i> parameter  can be one of the following types.

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
Signed long data.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_DATE"></a><a id="proptype_date"></a><dl>
<dt><b>PROPTYPE_DATE</b></dt>
</dl>
</td>
<td width="60%">
Date/time.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_BINARY"></a><a id="proptype_binary"></a><dl>
<dt><b>PROPTYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary data.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_STRING"></a><a id="proptype_string"></a><dl>
<dt><b>PROPTYPE_STRING</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/u-gly">Unicode</a> string data.

</td>
</tr>
</table>

### -param pvarPropertyValue [out]

A pointer to the <b>VARIANT</b> that contains the request property type.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and  the <i>pvarPropertyValue</i> parameter contains the  request property.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the request property.

## -remarks

The 
<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">SetContext</a> method must be called prior to calling this method. The call to <b>SetContext</b> specifies which request is used as the current context.

Requests  hold all the associated states for the request and the eventual granted certificate that is not a part of the certificate. Thus, data such as revocation times and disposition data are kept in the request data object.

The <b>RequestType</b> property can be set to one of the following values.<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>CR_IN_PKCS</td>
<td>The request is a PKCS #7 renewal or registration request.</td>
</tr>
<tr>
<td>CR_IN-PKCS10</td>
<td>The request is a PKCS #10 request.</td>
</tr>
<tr>
<td>CR_IN_KEYGEN</td>
<td>The request is a Keygen request (Netscape format).</td>
</tr>
</table>
 




#### Examples


```cpp
BSTR      bstrPropName = NULL;
VARIANT   varProp;

VariantInit( &varProp );

bstrPropName = SysAllocString(L"RequestID");

// Retrieve the request property.
// pCertServerPolicy has been used to call SetContext previously.
hr = pCertServerPolicy->GetRequestProperty( bstrPropName,
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

<a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">ICertServerPolicy::SetContext</a>



<a href="/windows/desktop/SecCrypto/name-properties">Name Properties</a>