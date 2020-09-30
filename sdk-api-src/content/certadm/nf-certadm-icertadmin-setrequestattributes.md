---
UID: NF:certadm.ICertAdmin.SetRequestAttributes
title: ICertAdmin::SetRequestAttributes (certadm.h)
description: Sets attributes in the specified pending certificate request. This method was first defined in the ICertAdmin interface.
helpviewer_keywords: ["CCertAdmin interface [Security]","SetRequestAttributes method","ICertAdmin interface [Security]","SetRequestAttributes method","ICertAdmin.SetRequestAttributes","ICertAdmin2 interface [Security]","SetRequestAttributes method","ICertAdmin2::SetRequestAttributes","ICertAdmin::SetRequestAttributes","SetRequestAttributes","SetRequestAttributes method [Security]","SetRequestAttributes method [Security]","CCertAdmin interface","SetRequestAttributes method [Security]","ICertAdmin interface","SetRequestAttributes method [Security]","ICertAdmin2 interface","certadm/ICertAdmin2::SetRequestAttributes","certadm/ICertAdmin::SetRequestAttributes","security.icertadmin2_setrequestattributes"]
old-location: security\icertadmin2_setrequestattributes.htm
tech.root: security
ms.assetid: 309c53f9-50cf-4c50-bc48-a4f15a8ced18
ms.date: 12/05/2018
ms.keywords: CCertAdmin interface [Security],SetRequestAttributes method, ICertAdmin interface [Security],SetRequestAttributes method, ICertAdmin.SetRequestAttributes, ICertAdmin2 interface [Security],SetRequestAttributes method, ICertAdmin2::SetRequestAttributes, ICertAdmin::SetRequestAttributes, SetRequestAttributes, SetRequestAttributes method [Security], SetRequestAttributes method [Security],CCertAdmin interface, SetRequestAttributes method [Security],ICertAdmin interface, SetRequestAttributes method [Security],ICertAdmin2 interface, certadm/ICertAdmin2::SetRequestAttributes, certadm/ICertAdmin::SetRequestAttributes, security.icertadmin2_setrequestattributes
req.header: certadm.h
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
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertAdmin::SetRequestAttributes
 - certadm/ICertAdmin::SetRequestAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.SetRequestAttributes
 - ICertAdmin.SetRequestAttributes
 - CCertAdmin.SetRequestAttributes
---

# ICertAdmin::SetRequestAttributes


## -description

The <b>SetRequestAttributes</b> method sets attributes in the specified pending <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. This method was first defined in the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> interface.

For this method to succeed, the certificate request must be pending.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) server in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the network name of the Certificate Services server and CANAME is the common name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>SetRequestAttributes</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param RequestId [in]

Specifies the ID of the request receiving the <a href="/windows/desktop/SecGloss/a-gly">attributes</a>.

### -param strAttributes [in]

Specifies the attribute data. Each attribute is a name-value string pair. The colon character separates the name and value, and a newline character separates multiple name-value pairs, for example:

<table>
<tr>
<td><strong>C++</strong></td>
<td>
<i>AttributeName1</i><b>:</b><i>AttributeValue1</i><b>\</b><i>nAttributeName2</i><b>:</b><i>AttributeValue2</i>

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
<i>AttributeName1</i><b>:</b><i>AttributeValue1</i><b> &amp; </b><i>vbNewLine</i><b> &amp; </b><i>AttributeName2</i><b>:</b><i>AttributeValue2</i>

</td>
</tr>
</table>
There is no set limit to the number of request attributes that may be added to a request.

When Certificate Services parses attribute names, it ignores spaces, hyphens (minus signs), and case. For example, <i>AttributeName1</i>, <i>Attribute Name1</i>, and <i>Attribute-name1</i> are all equivalent. For attribute values, Certificate Services ignores leading and trailing white space.

<div class="alert"><b>Note</b>  The maximum length for an attribute name is 127 non-<b>NULL</b> characters. The maximum length for an attribute value is 4,096 non-<b>NULL</b> characters.</div>
<div> </div>

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

<a href="/windows/desktop/SecGloss/a-gly">Attributes</a> added or updated by calling <b>SetRequestAttributes</b> do not alter the initial, unparsed attribute string associated with the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. The certificate request's unparsed attribute string is unalterable after the certificate is requested (the 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-submit">ICertRequest::Submit</a> method allows attributes to be specified at the time the certificate is requested).

You can use the Certification Authority MMC snap-in to display the initial unparsed request attribute string.

When you view the parsed attributes, you will also see any changes due to calls to <b>SetRequestAttributes</b>.

<p class="proch"><b>To view the parsed attributes</b>

<ol>
<li>Open the Certification Authority MMC snap-in.</li>
<li>Open the <b>Pending Requests</b> folder.</li>
<li>Right-click a request, point to <b>All Tasks</b>, and then click <b>View Attributes/Extensions</b>.</li>
</ol>
  To enumerate or view all of the parsed attributes, including those added by means of <b>SetRequestAttributes</b>, you may also use the 
<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">IEnumCERTVIEWATTRIBUTE</a> interface.

Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.


#### Examples


```cpp
    BSTR bstrAttribs = NULL;
    BSTR bstrCA = NULL;
    long nReqID;  // request ID

    //  Specify the attributes.
    //  For example, "AttName1:AttValue1\nAttName2:AttValue2". 
    bstrAttribs = SysAllocString(L"<ATTRIBUTESHERE>");
    if (NULL == bstrAttribs)
    {
        printf("Memory allocation failed for bstrAttribs.\n");
        goto error;
    }
    
    bstrCA = SysAllocString(L"<COMPUTERNAMEHERE>\\<CANAMEHERE>");
    if (NULL == bstrCA)
    {
        printf("Memory allocation failed for bstrCA.\n");
        goto error;
    }

    //  Request ID to receive the attributes.
    nReqID = <REQUESTIDHERE>;

    //  Add these attributes to the certificate.
    //  pCertAdmin is a previously instantiated
    //  ICertAdmin object pointer. 
    hr = pCertAdmin->SetRequestAttributes( bstrCA,
                                           nReqID,
                                           bstrAttribs );
    if (FAILED(hr))
        printf("Failed SetRequestAttributes [%x]\n", hr);
    else
        printf("SetRequestAttributes succeeded\n");

    //  Done processing.

error:

    if (bstrAttribs)
        SysFreeString(bstrAttribs);
    if (bstrCA)
        SysFreeString(bstrCA);
    //  Free other resources.
```

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">CCertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certview/nn-certview-ienumcertviewattribute">IEnumCERTVIEWATTRIBUTE</a>