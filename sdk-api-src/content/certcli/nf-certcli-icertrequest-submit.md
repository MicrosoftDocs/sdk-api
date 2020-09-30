---
UID: NF:certcli.ICertRequest.Submit
title: ICertRequest::Submit (certcli.h)
description: Submits a request to the Certificate Services server.
helpviewer_keywords: ["CCertRequest object [Security]","Submit method","CR_IN_BASE64","CR_IN_BASE64HEADER","CR_IN_BINARY","CR_IN_CHALLENGERESPONSE","CR_IN_CLIENTIDNONE","CR_IN_CMC","CR_IN_CONNECTONLY","CR_IN_CRLS","CR_IN_ENCODEANY","CR_IN_FORMATANY","CR_IN_FULLRESPONSE","CR_IN_KEYGEN","CR_IN_MACHINE","CR_IN_PKCS10","CR_IN_PKCS7","CR_IN_RETURNCHALLENGE","CR_IN_ROBO","CR_IN_RPC","ICertRequest interface [Security]","Submit method","ICertRequest.Submit","ICertRequest2 interface [Security]","Submit method","ICertRequest2::Submit","ICertRequest3 interface [Security]","Submit method","ICertRequest3::Submit","ICertRequest::Submit","Submit","Submit method [Security]","Submit method [Security]","CCertRequest object","Submit method [Security]","ICertRequest interface","Submit method [Security]","ICertRequest2 interface","Submit method [Security]","ICertRequest3 interface","certcli/ICertRequest2::Submit","certcli/ICertRequest3::Submit","certcli/ICertRequest::Submit","security.icertrequest2_submit"]
old-location: security\icertrequest2_submit.htm
tech.root: security
ms.assetid: 22ae8d39-3f16-4f7d-94a0-aa68b03aaa0b
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],Submit method, CR_IN_BASE64, CR_IN_BASE64HEADER, CR_IN_BINARY, CR_IN_CHALLENGERESPONSE, CR_IN_CLIENTIDNONE, CR_IN_CMC, CR_IN_CONNECTONLY, CR_IN_CRLS, CR_IN_ENCODEANY, CR_IN_FORMATANY, CR_IN_FULLRESPONSE, CR_IN_KEYGEN, CR_IN_MACHINE, CR_IN_PKCS10, CR_IN_PKCS7, CR_IN_RETURNCHALLENGE, CR_IN_ROBO, CR_IN_RPC, ICertRequest interface [Security],Submit method, ICertRequest.Submit, ICertRequest2 interface [Security],Submit method, ICertRequest2::Submit, ICertRequest3 interface [Security],Submit method, ICertRequest3::Submit, ICertRequest::Submit, Submit, Submit method [Security], Submit method [Security],CCertRequest object, Submit method [Security],ICertRequest interface, Submit method [Security],ICertRequest2 interface, Submit method [Security],ICertRequest3 interface, certcli/ICertRequest2::Submit, certcli/ICertRequest3::Submit, certcli/ICertRequest::Submit, security.icertrequest2_submit
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
 - ICertRequest::Submit
 - certcli/ICertRequest::Submit
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
 - ICertRequest3.Submit
 - ICertRequest2.Submit
 - ICertRequest.Submit
 - CCertRequest.Submit
---

# ICertRequest::Submit


## -description

The <b>Submit</b> method submits a request to the Certificate Services server.

If the resulting disposition status is CR_DISP_ISSUED, you can retrieve the issued certificate by calling 
the <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-getcertificate">ICertRequest3::GetCertificate</a> method.

## -parameters

### -param Flags [in]

Specifies the request format, type of request, and whether the request is encrypted. One of the following format attribute flags can be used to specify how the request is encoded. 




               



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_IN_BASE64"></a><a id="cr_in_base64"></a><dl>
<dt><b>CR_IN_BASE64</b></dt>
</dl>
</td>
<td width="60%">
Unicode BASE64 format without begin/end.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_BASE64HEADER"></a><a id="cr_in_base64header"></a><dl>
<dt><b>CR_IN_BASE64HEADER</b></dt>
</dl>
</td>
<td width="60%">
Unicode BASE64 format with begin/end.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_BINARY"></a><a id="cr_in_binary"></a><dl>
<dt><b>CR_IN_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary format.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_ENCODEANY"></a><a id="cr_in_encodeany"></a><dl>
<dt><b>CR_IN_ENCODEANY</b></dt>
</dl>
</td>
<td width="60%">
Try all of the CR_IN_BASE64HEADER, CR_IN_BASE64, or CR_IN_BINARY formats.

</td>
</tr>
</table>
 

One of the following format value flags can be used to specify the type of the request.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_IN_RETURNCHALLENGE"></a><a id="cr_in_returnchallenge"></a><dl>
<dt><b>CR_IN_RETURNCHALLENGE</b></dt>
</dl>
</td>
<td width="60%">
Return a challenge that can be submitted to a CA. The challenge is a <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC)  full request. When this flag is turned on, calling the <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest2-getfullresponseproperty">GetFullResponseProperty</a> method with the FR_PROP_FULLRESPONSE flag returns a CMC response that contains key attestation challenge.


</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_CHALLENGERESPONSE"></a><a id="cr_in_challengeresponse"></a><dl>
<dt><b>CR_IN_CHALLENGERESPONSE</b></dt>
</dl>
</td>
<td width="60%">
The call is a response to a challenge. The RequestId must be passed in the <i>strAttributes</i> parameter and the response to the challenge must be passed in the <i>strRequest</i> parameter.  This flag should be turned on when an application needs to send back the decrypted challenge to the CA. You can then call the <a href="/windows/desktop/api/certcli/nf-certcli-icertrequest2-getfullresponseproperty">GetFullResponseProperty</a> method to get the issued end entity certificate.


</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_CMC"></a><a id="cr_in_cmc"></a><dl>
<dt><b>CR_IN_CMC</b></dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) request.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_FORMATANY"></a><a id="cr_in_formatany"></a><dl>
<dt><b>CR_IN_FORMATANY</b></dt>
</dl>
</td>
<td width="60%">
Try all of the CR_IN_CMC, CR_IN_KEYGEN, CR_IN_PKCS7,  or CR_IN_PKCS10 formats.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_KEYGEN"></a><a id="cr_in_keygen"></a><dl>
<dt><b>CR_IN_KEYGEN</b></dt>
</dl>
</td>
<td width="60%">
Keygen request (Netscape format).

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_PKCS7"></a><a id="cr_in_pkcs7"></a><dl>
<dt><b>CR_IN_PKCS7</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/p-gly">PKCS #7</a> request (renewal or registration agent).

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_PKCS10"></a><a id="cr_in_pkcs10"></a><dl>
<dt><b>CR_IN_PKCS10</b></dt>
</dl>
</td>
<td width="60%">
PKCS #10 request.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_RPC"></a><a id="cr_in_rpc"></a><dl>
<dt><b>CR_IN_RPC</b></dt>
</dl>
</td>
<td width="60%">
Transmit the messages using RPC instead of DCOM.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_FULLRESPONSE"></a><a id="cr_in_fullresponse"></a><dl>
<dt><b>CR_IN_FULLRESPONSE</b></dt>
</dl>
</td>
<td width="60%">
Return a full CMC response.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_CRLS"></a><a id="cr_in_crls"></a><dl>
<dt><b>CR_IN_CRLS</b></dt>
</dl>
</td>
<td width="60%">
Include the current certificate revocation lists.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_MACHINE"></a><a id="cr_in_machine"></a><dl>
<dt><b>CR_IN_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
Use the context of the key service computer.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_ROBO"></a><a id="cr_in_robo"></a><dl>
<dt><b>CR_IN_ROBO</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the message is being requested on behalf of another sender.

If the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) is not configured for "renew on behalf of", then the CA rejects the request.
 

For more information about enabling "renew on behalf of" on the CA, see <a href="/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759245(v=ws.11)">Configuring the Certificate Enrollment Web Service for Renewal Only Mode</a>.

The request must be a renewal request and the signing certificate must be using the same template as the request.

In addition, the request will succeed only when one of the following conditions is true:

<ul>
<li>The signing certificate must have been issued by the same CA</li>
<li>The signing certificate's SAN2 extension has the UPN of the subject</li>
<li>The signing certificate's Subject Name has the FQDN_1779 of the subject</li>
</ul>
<b>Windows Server 2008 and Windows Server 2003:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_CLIENTIDNONE"></a><a id="cr_in_clientidnone"></a><dl>
<dt><b>CR_IN_CLIENTIDNONE</b></dt>
</dl>
</td>
<td width="60%">
Do not include in the request data that identifies the client.

<b>Windows Server 2008 and Windows Server 2003:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_IN_CONNECTONLY"></a><a id="cr_in_connectonly"></a><dl>
<dt><b>CR_IN_CONNECTONLY</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the DCOM connection with the server is established, but the request is not  submitted.

</td>
</tr>
</table>

### -param strRequest [in]

A pointer to the string that contains the <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. If CR_IN_BASE64 or CR_IN_BASE64HEADER was specified in <i>Flags</i>, <i>strRequest</i> must be a Unicode string.

### -param strAttributes [in]

A pointer to the string that contains optional extra <a href="/windows/desktop/SecGloss/a-gly">attributes</a> for the request. Each attribute is a name-value string pair. The colon character separates the name and value, and a newline character separates multiple name-value pairs, for example:

<table>
<tr>
<td><strong>C++</strong></td>
<td>
 "AttributeName1:AttributeValue1\nAttributeName2:AttributeValue2"

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
 "AttributeName1:AttributeValue1" &amp; vbNewLine &amp; "AttributeName2:AttributeValue2"

</td>
</tr>
</table>
When Certificate Services server parses attribute names, it ignores spaces, hyphens (minus signs), and case. For example, "AttributeName1", "Attribute Name1", and "Attribute-name1" are all equivalent. For attribute values, Certificate Services server ignores leading and trailing white space.

### -param strConfig [in]

Represents a valid configuration string for the Certificate Services server. The string can be either an HTTPS URL for an enrollment server or in the form <i>ComputerName</i><b>\\</b><i>CAName</i>, where <i>ComputerName</i> is the network name of the server, and <i>CAName</i> is the common name of the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>An HTTPS URL is not supported as an input.

### -param pDisposition [out, retval]

A pointer to the request's disposition value.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

 Upon successful completion of this function, *<i>pDisposition</i> is set to one of the values in the following table.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value specifies the disposition of the request. The disposition is one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Request denied

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Request failed

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Request did not complete

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ISSUED</b></dt>
</dl>
</td>
<td width="60%">
Certificate issued

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ISSUED_OUT_OF_BAND</b></dt>
</dl>
</td>
<td width="60%">
Certificate issued separately

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_UNDER_SUBMISSION</b></dt>
</dl>
</td>
<td width="60%">
Request taken under submission

</td>
</tr>
</table>

## -remarks

If you read a BASE64 format request from a file, ensure that the file is in Unicode, or convert it from ASCII to Unicode before submitting the request with this method.


#### Examples


```cpp
    //  The pointer to the interface object.
    ICertRequest * pCertRequest = NULL;

    //  The variable for the computer\CAName.
    BSTR         bstrCA = NULL;

    //  The variable for the request.
    BSTR         bstrRequest = NULL;

    //  The variable for the attributes.
    BSTR         bstrAttribs = NULL;

    //  The variable for the disposition code.
    long        nDisp;

    HRESULT     hr;

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

    //  Check status.
    if (FAILED(hr))
    {
        printf("Failed CoInitializeEx [%x]\n", hr);
        goto error;
    }

    //  Instantiate the CertConfig object.
    hr = CoCreateInstance(CLSID_CCertRequest,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_ICertRequest,
                          (void **)&pCertRequest);
    if (FAILED(hr))
    {
        printf("Failed CoCreateInstance pCertRequest [%x]\n", hr);
        goto error;
    }

    //  Specify the certification authority.
    //  Note: In C++, produce one backslash (\) by using two.
    bstrCA = SysAllocString(L"server01\\myCAName");

    //  Create the request (not shown), and assign it to bstrRequest,
    //  for example, use ICEnroll::createPKCS10.

    //  Generate the attributes. In this case, no attributes
    //  are specified.
    bstrAttribs = SysAllocString(L"");
    
    //  Submit the request.
    hr = pCertRequest->Submit(CR_IN_BASE64 | CR_IN_PKCS10, 
                              bstrRequest,
                              bstrAttribs,
                              bstrCA, 
                              &nDisp );
    if (FAILED(hr))
    {
        printf("Failed Submit [%x]\n", hr);
        goto error;
    }
    else
    {
        //  Use the disposition value as needed.
    }

    //  Done processing.

error:

    //  Free BSTR values.
    if (NULL != bstrCA)
        SysFreeString(bstrCA);

    if (NULL != bstrRequest)
        SysFreeString(bstrRequest);

    if (NULL != bstrAttribs)
        SysFreeString(bstrAttribs);

    //  Clean up object resources.
    if (NULL != pCertRequest)
        pCertRequest->Release();

    //  Free COM resources.
    CoUninitialize();

```

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">CCertRequest</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-createpkcs10">ICEnroll::createPKCS10</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest3">ICertRequest3</a>