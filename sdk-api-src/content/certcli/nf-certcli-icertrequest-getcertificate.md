---
UID: NF:certcli.ICertRequest.GetCertificate
title: ICertRequest::GetCertificate (certcli.h)
description: Returns the certificate issued for the request as an X.509 certificate, or optionally packaged in a Public Key Cryptography Standards (PKCS)
helpviewer_keywords: ["CCertRequest object [Security]","GetCertificate method","CR_OUT_BASE64","CR_OUT_BASE64HEADER","CR_OUT_BINARY","CR_OUT_CHAIN","CR_OUT_CRLS","GetCertificate","GetCertificate method [Security]","GetCertificate method [Security]","CCertRequest object","GetCertificate method [Security]","ICertRequest interface","GetCertificate method [Security]","ICertRequest2 interface","GetCertificate method [Security]","ICertRequest3 interface","ICertRequest interface [Security]","GetCertificate method","ICertRequest.GetCertificate","ICertRequest2 interface [Security]","GetCertificate method","ICertRequest2::GetCertificate","ICertRequest3 interface [Security]","GetCertificate method","ICertRequest3::GetCertificate","ICertRequest::GetCertificate","certcli/ICertRequest2::GetCertificate","certcli/ICertRequest3::GetCertificate","certcli/ICertRequest::GetCertificate","security.icertrequest2_getcertificate"]
old-location: security\icertrequest2_getcertificate.htm
tech.root: security
ms.assetid: ba8fc725-c376-4e66-8417-777ce13f2954
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],GetCertificate method, CR_OUT_BASE64, CR_OUT_BASE64HEADER, CR_OUT_BINARY, CR_OUT_CHAIN, CR_OUT_CRLS, GetCertificate, GetCertificate method [Security], GetCertificate method [Security],CCertRequest object, GetCertificate method [Security],ICertRequest interface, GetCertificate method [Security],ICertRequest2 interface, GetCertificate method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetCertificate method, ICertRequest.GetCertificate, ICertRequest2 interface [Security],GetCertificate method, ICertRequest2::GetCertificate, ICertRequest3 interface [Security],GetCertificate method, ICertRequest3::GetCertificate, ICertRequest::GetCertificate, certcli/ICertRequest2::GetCertificate, certcli/ICertRequest3::GetCertificate, certcli/ICertRequest::GetCertificate, security.icertrequest2_getcertificate
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
 - ICertRequest::GetCertificate
 - certcli/ICertRequest::GetCertificate
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
 - ICertRequest3.GetCertificate
 - ICertRequest2.GetCertificate
 - ICertRequest.GetCertificate
 - CCertRequest.GetCertificate
---

# ICertRequest::GetCertificate


## -description

The <b>GetCertificate</b> method returns the certificate issued for the request as an <a href="/windows/desktop/SecGloss/x-gly">X.509</a> certificate, or optionally packaged in a <a href="/windows/desktop/SecGloss/p-gly">Public Key Cryptography Standards</a> (PKCS) #7 message that contains the complete certificate chain for the <a href="/windows/desktop/SecGloss/c-gly">Certificate Services</a> server.

## -parameters

### -param Flags [in]

A flag for the format and  whether the complete certificate chain is included.


The format of the returned certificate
                  can be one of the following flags.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BASE64HEADER"></a><a id="cr_out_base64header"></a><dl>
<dt><b>CR_OUT_BASE64HEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 format with begin/end

</td>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BASE64"></a><a id="cr_out_base64"></a><dl>
<dt><b>CR_OUT_BASE64</b></dt>
</dl>
</td>
<td width="60%">
BASE64 format without begin/end

</td>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BINARY"></a><a id="cr_out_binary"></a><dl>
<dt><b>CR_OUT_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary format

</td>
</tr>
</table>
 


The following flags can be combined with the format flag.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_CHAIN"></a><a id="cr_out_chain"></a><dl>
<dt><b>CR_OUT_CHAIN</b></dt>
</dl>
</td>
<td width="60%">
Include complete certificate chain in the PKCS #7.

 If this flag is not specified, only the requested certificate, in <a href="/windows/desktop/SecGloss/x-gly">X.509</a> format, is returned.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_CRLS"></a><a id="cr_out_crls"></a><dl>
<dt><b>CR_OUT_CRLS</b></dt>
</dl>
</td>
<td width="60%">
Include <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs) in the PKCS #7.

</td>
</tr>
</table>
 

For example, to retrieve a binary certificate with complete certificate chain in C++ you would write the following.


``` syntax
hResult = pCertReq->GetCACertificate(FALSE, bstrConfig,
     CR_OUT_BINARY | CR_OUT_CHAIN, &bstrCert);
```


### -param pstrCertificate [out]

A pointer to the <b>BSTR</b> that contains the certificate, in the specified format.

When using this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and then pass the address of this variable as <i>pstrCertificate</i>. When you have finished using the certificate pointed to by <i>pstrCertificate</i>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

If the method sets *<i>pstrCertificate</i>  to the <b>BSTR</b> that contains the certificate for the request, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

An application would call this method to retrieve the certificate issued by means of an earlier call to 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-submit">ICertRequest3::Submit</a> or 
<a href="/windows/desktop/api/certcli/nf-certcli-icertrequest-retrievepending">ICertRequest3::RetrievePending</a>.


#### Examples

The following example shows retrieving a certificate.


```cpp
#include <windows.h>
#include <stdio.h>
#include <Certcli.h>

HRESULT main()
{
    //  Pointer to interface object.
    ICertRequest * pCertRequest = NULL;

    //  Variable for COMPUTER\CANAME.
    BSTR         bstrCA = NULL;

    //  Variable for CA Certificate.
    BSTR         bstrCACert = NULL;

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

    //  Note use of two backslashes (\\) in C++ 
    //  to produce one backslash (\).
    bstrCA = SysAllocString(L"server01\\myCAName");
    
    //  Retrieve the CA certificate.
    hr = pCertRequest->GetCACertificate(FALSE,
                                        bstrCA,
                                        CR_OUT_BASE64,
                                        &bstrCACert);
    if (FAILED(hr))
    {
        printf("Failed GetCACertificate [%x]\n", hr);
        goto error;
    }
    else
    {
        //  Use CA Certificate as needed.
    }

    //  Done processing.

error:

    //  Free BSTR values.
    if (NULL != bstrCA)
        SysFreeString(bstrCA);

    if (NULL != bstrCACert)
        SysFreeString(bstrCACert);

    //  Clean up object resources.
    if (NULL != pCertRequest)
        pCertRequest->Release();

    //  Free COM resources.
    CoUninitialize();

    return hr;

}

```

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">CCertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest3">ICertRequest3</a>
