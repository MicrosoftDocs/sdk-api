---
UID: NF:certif.ICertServerPolicy.SetCertificateProperty
title: ICertServerPolicy::SetCertificateProperty (certif.h)
description: To set a property associated with a certificate.
helpviewer_keywords: ["CCertServerPolicy object [Security]","SetCertificateProperty method","CrossForest","GeneralFlags","ICertServerPolicy interface [Security]","SetCertificateProperty method","ICertServerPolicy.SetCertificateProperty","ICertServerPolicy::SetCertificateProperty","NotAfter","NotBefore","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","RequesterDN","RequesterSAMName","RequesterUPN","SetCertificateProperty","SetCertificateProperty method [Security]","SetCertificateProperty method [Security]","CCertServerPolicy object","SetCertificateProperty method [Security]","ICertServerPolicy interface","_certsrv_icertserverpolicy_setcertificateproperty","certif/ICertServerPolicy::SetCertificateProperty","security.icertserverpolicy_setcertificateproperty"]
old-location: security\icertserverpolicy_setcertificateproperty.htm
tech.root: security
ms.assetid: 1230aa79-d8b0-4f2b-ab10-412b8c530b0b
ms.date: 12/05/2018
ms.keywords: CCertServerPolicy object [Security],SetCertificateProperty method, CrossForest, GeneralFlags, ICertServerPolicy interface [Security],SetCertificateProperty method, ICertServerPolicy.SetCertificateProperty, ICertServerPolicy::SetCertificateProperty, NotAfter, NotBefore, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, RequesterDN, RequesterSAMName, RequesterUPN, SetCertificateProperty, SetCertificateProperty method [Security], SetCertificateProperty method [Security],CCertServerPolicy object, SetCertificateProperty method [Security],ICertServerPolicy interface, _certsrv_icertserverpolicy_setcertificateproperty, certif/ICertServerPolicy::SetCertificateProperty, security.icertserverpolicy_setcertificateproperty
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
 - ICertServerPolicy::SetCertificateProperty
 - certif/ICertServerPolicy::SetCertificateProperty
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
 - ICertServerPolicy.SetCertificateProperty
 - CCertServerPolicy.SetCertificateProperty
---

# ICertServerPolicy::SetCertificateProperty


## -description

Use the <b>SetCertificateProperty</b> method to set a property associated with a certificate.

## -parameters

### -param strPropertyName [in]

Specifies the property to set. You can set any of the 
<a href="/windows/desktop/SecCrypto/name-properties">Name Properties</a> associated with the certificate. 


 In addition, you can set the following certificate properties.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NotBefore"></a><a id="notbefore"></a><a id="NOTBEFORE"></a><dl>
<dt><b>NotBefore</b></dt>
<dt>Date/time</dt>
</dl>
</td>
<td width="60%">
The certificate is not valid before the given date.

</td>
</tr>
<tr>
<td width="40%"><a id="NotAfter"></a><a id="notafter"></a><a id="NOTAFTER"></a><dl>
<dt><b>NotAfter</b></dt>
<dt>Date/time</dt>
</dl>
</td>
<td width="60%">
The certificate is not valid after the given date.

</td>
</tr>
<tr>
<td width="40%"><a id="GeneralFlags"></a><a id="generalflags"></a><a id="GENERALFLAGS"></a><dl>
<dt><b>GeneralFlags</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
 Set this property to 0x00000400 to prevent the request from being persisted in the CA database.

<div class="alert"><b>Caution</b>  Do not overwrite any mask values returned by <a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-getcertificateproperty">GetCertificateProperty</a> when setting this property. Set the value by performing a bitwise <b>OR</b> with the existing values.</div>
<div> </div>
<b>Windows Storage Server 2003:  </b>This field is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CrossForest"></a><a id="crossforest"></a><a id="CROSSFOREST"></a><dl>
<dt><b>CrossForest</b></dt>
<dt>PROPTYPE_LONG</dt>
</dl>
</td>
<td width="60%">
A Boolean value that specifies whether the CA should operate cross forest enrollment 								mode.

<b>Windows Server 2008 and Windows Server 2003:  </b>Cross forest enrollment is not supported. Cross forest enrollment is supported beginning with Windows Server 2008 R2.

</td>
</tr>
<tr>
<td width="40%"><a id="RequesterSAMName"></a><a id="requestersamname"></a><a id="REQUESTERSAMNAME"></a><dl>
<dt><b>RequesterSAMName</b></dt>
<dt>PROPTYPE_STRING</dt>
</dl>
</td>
<td width="60%">
Tells the CA to set the requester account name ("RequesterName") and distinguished 								name.

</td>
</tr>
<tr>
<td width="40%"><a id="RequesterUPN"></a><a id="requesterupn"></a><a id="REQUESTERUPN"></a><dl>
<dt><b>RequesterUPN</b></dt>
<dt>PROPTYPE_STRING</dt>
</dl>
</td>
<td width="60%">
Tells the CA to convert the <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN) of the requester to the requester 								name ("RequesterName")  and to set the requester name and the requester distinguished 								name.

</td>
</tr>
<tr>
<td width="40%"><a id="RequesterDN"></a><a id="requesterdn"></a><a id="REQUESTERDN"></a><dl>
<dt><b>RequesterDN</b></dt>
<dt>PROPTYPE_STRING</dt>
</dl>
</td>
<td width="60%">
Tells the CA to convert the FQDN 1779 name of the requester to the requester 										name and to set the requester name ("RequesterName")  and the requester  distinguished 								name.

</td>
</tr>
</table>

### -param PropertyType [in]

Specifies the type of the property being set. The <i>Type</i> parameter must agree with the data type of <i>pvarValue</i> that is set in the <b>vt</b> field of the <b>VARIANT</b> structure. The <i>Type</i> parameter can be set to one of the following types.

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
Date/time data.

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
<a href="/windows/desktop/SecGloss/u-gly">Unicode</a> string data

</td>
</tr>
</table>

### -param pvarPropertyValue [in]

Specifies the value to set the property to.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

You must call 
<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">ICertServerPolicy::SetContext</a> prior to using this method.

The NotBefore and NotAfter certificate properties constrain the lifetime during which a certificate is valid. The data type for these properties is a floating-point <b>VARIANT</b> date derived from COleDateTime in Automation.

The following restrictions apply when setting the NotBefore and NotAfter certificate properties with <b>SetCertificateProperty</b>:

<ul>
<li>The NotBefore date cannot be set to a date earlier than the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) certificate's NotBefore date.</li>
<li>The NotAfter date cannot be set to a date later than the CA certificate's NotAfter date.</li>
<li>The NotBefore date cannot be set to a date earlier than it already is set, even if the new date is later than the CA certificate's NotBefore date.</li>
<li>The NotAfter date cannot be set to a date later than it already is set, even if the new date is before the CA certificate's NotAfter date.</li>
</ul>

#### Examples

The following example calls the <b>SetCertificateProperty</b> method to set the NotBefore certificate property. The example assumes pServer is valid and the <a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">ICertServerPolicy::SetContext</a> method has been called.


```cpp
HRESULT hr;
ICertServerPolicy *pServer;
SYSTEMTIME st;
BSTR bstrPropName;
VARIANT vPropValue;

bstrPropName = SysAllocString(L"NotBefore");
if (NULL == bstrPropName)
{
    printf("Unable to allocate memory.\n"); 
    return E_OUTOFMEMORY;
}

// Set the 'NotBefore' property to Noon on Jan. 1, 2000.
memset( &st, 0, sizeof(SYSTEMTIME));
st.wYear = 2000;
st.wMonth = 1;     // Jan.
st.wDay = 1;       // 1st day of month.
st.wHour = 12;     // Noon.

// Place the date into VARIANT required format.
VariantInit( &vPropValue );
vPropValue.vt = VT_DATE;
if ( !SystemTimeToVariantTime( &st, &vPropValue.date))
{
    printf("Unable to convert time.\n");
    SysFreeString(bstrPropName);
    return E_FAIL
}

// Set the NotBefore property in the certificate:
hr = pServer->SetCertificateProperty(bstrPropName,
                                     PROPTYPE_DATE, 
                                     &vPropValue);
SysFreeString(bstrPropName);
VariantClear(&vPropValue);
if (FAILED(hr))
{
    printf("SetCertificateProperty failed [%x]\n", hr);
    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-getcertificateproperty">ICertServerExit::GetCertificateProperty</a>



<a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">ICertServerPolicy::SetContext</a>



<a href="/windows/desktop/SecCrypto/name-properties">Name Properties</a>