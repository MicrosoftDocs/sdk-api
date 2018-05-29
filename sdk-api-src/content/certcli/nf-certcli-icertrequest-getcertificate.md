---
UID: NF:certcli.ICertRequest.GetCertificate
title: ICertRequest::GetCertificate
author: windows-sdk-content
description: Returns the certificate issued for the request as an X.509 certificate, or optionally packaged in a Public Key Cryptography Standards (PKCS) #7 message that contains the complete certificate chain for the Certificate Services server.
old-location: security\icertrequest2_getcertificate.htm
old-project: SecCrypto
ms.assetid: ba8fc725-c376-4e66-8417-777ce13f2954
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CCertRequest object [Security],GetCertificate method, CR_OUT_BASE64, CR_OUT_BASE64HEADER, CR_OUT_BINARY, CR_OUT_CHAIN, CR_OUT_CRLS, GetCertificate, GetCertificate method [Security], GetCertificate method [Security],CCertRequest object, GetCertificate method [Security],ICertRequest interface, GetCertificate method [Security],ICertRequest2 interface, GetCertificate method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetCertificate method, ICertRequest.GetCertificate, ICertRequest2 interface [Security],GetCertificate method, ICertRequest2::GetCertificate, ICertRequest3 interface [Security],GetCertificate method, ICertRequest3::GetCertificate, ICertRequest::GetCertificate, certcli/ICertRequest2::GetCertificate, certcli/ICertRequest3::GetCertificate, certcli/ICertRequest::GetCertificate, security.icertrequest2_getcertificate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: X509EnrollmentAuthFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certcli.dll
api_name:
-	ICertRequest3.GetCertificate
-	ICertRequest2.GetCertificate
-	ICertRequest.GetCertificate
-	CCertRequest.GetCertificate
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
---

# ICertRequest::GetCertificate


## -description


The <b>GetCertificate</b> method returns the certificate issued for the request as an <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> certificate, or optionally packaged in a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">Public Key Cryptography Standards</a> (PKCS) #7 message that contains the complete certificate chain for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Services</a> server.


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

 If this flag is not specified, only the requested certificate, in <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> format, is returned.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_CRLS"></a><a id="cr_out_crls"></a><dl>
<dt><b>CR_OUT_CRLS</b></dt>
</dl>
</td>
<td width="60%">
Include <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation lists</a> (CRLs) in the PKCS #7.

</td>
</tr>
</table>
 

For example, to retrieve a binary certificate with complete certificate chain in C++ you would write the following.

<pre class="syntax" xml:space="preserve"><code>hResult = pCertReq-&gt;GetCACertificate(FALSE, bstrConfig,
     CR_OUT_BINARY | CR_OUT_CHAIN, &amp;bstrCert);</code></pre>

### -param pstrCertificate [out]

A pointer to the <b>BSTR</b> that contains the certificate, in the specified format.

When using this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and then pass the address of this variable as <i>pstrCertificate</i>. When you have finished using the certificate pointed to by <i>pstrCertificate</i>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



If the method sets *<i>pstrCertificate</i>  to the <b>BSTR</b> that contains the certificate for the request, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



An application would call this method to retrieve the certificate issued by means of an earlier call to 
<a href="https://msdn.microsoft.com/22ae8d39-3f16-4f7d-94a0-aa68b03aaa0b">ICertRequest3::Submit</a> or 
<a href="https://msdn.microsoft.com/07a9ac57-f90e-4c5c-b563-8aebbcf8f42e">ICertRequest3::RetrievePending</a>.


#### Examples

The following example shows retrieving a certificate.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;Certcli.h&gt;

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
                          (void **)&amp;pCertRequest);
    if (FAILED(hr))
    {
        printf("Failed CoCreateInstance pCertRequest [%x]\n", hr);
        goto error;
    }

    //  Note use of two backslashes (\\) in C++ 
    //  to produce one backslash (\).
    bstrCA = SysAllocString(L"server01\\myCAName");
    
    //  Retrieve the CA certificate.
    hr = pCertRequest-&gt;GetCACertificate(FALSE,
                                        bstrCA,
                                        CR_OUT_BASE64,
                                        &amp;bstrCACert);
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
        pCertRequest-&gt;Release();

    //  Free COM resources.
    CoUninitialize();

    return hr;

}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">CCertRequest</a>



<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">ICertRequest</a>



<a href="https://msdn.microsoft.com/8587a682-27a5-4f26-b4bb-7088e4e5d8d3">ICertRequest2</a>



<a href="https://msdn.microsoft.com/01de2ac0-4844-41a6-acef-e3e83b350393">ICertRequest3</a>
 

 

