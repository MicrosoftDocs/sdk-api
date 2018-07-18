---
UID: NF:certadm.ICertAdmin.GetCRL
title: ICertAdmin::GetCRL
author: windows-sdk-content
description: Retrieves the current certificate revocation list (CRL) for the Certificate Services certification authority (CA).
old-location: security\icertadmin2_getcrl.htm
old-project: seccrypto
ms.assetid: bdfc64dd-7446-4c44-997f-fa0086bfbb4f
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CCertAdmin object [Security],GetCRL method, CR_OUT_BASE64, CR_OUT_BASE64HEADER, CR_OUT_BINARY, GetCRL, GetCRL method [Security], GetCRL method [Security],CCertAdmin object, GetCRL method [Security],ICertAdmin interface, GetCRL method [Security],ICertAdmin2 interface, ICertAdmin interface [Security],GetCRL method, ICertAdmin.GetCRL, ICertAdmin2 interface [Security],GetCRL method, ICertAdmin2::GetCRL, ICertAdmin::GetCRL, certadm/ICertAdmin2::GetCRL, certadm/ICertAdmin::GetCRL, security.icertadmin2_getcrl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.GetCRL
 - ICertAdmin.GetCRL
 - CCertAdmin.GetCRL
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# ICertAdmin::GetCRL


## -description


The <b>GetCRL</b> method retrieves the current <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) for the Certificate Services <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA). This method was first defined in the <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a> interface.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the CA whose CRL you want to retrieve. This string is in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the network name of the Certificate Services server and CANAME is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see <a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>GetCRL</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param Flags [in]

Specifies the format of the returned CRL. This parameter can be one of the following flags.

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
BASE64 format with begin/end.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BASE64"></a><a id="cr_out_base64"></a><dl>
<dt><b>CR_OUT_BASE64</b></dt>
</dl>
</td>
<td width="60%">
BASE64 format without begin/end.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BINARY"></a><a id="cr_out_binary"></a><dl>
<dt><b>CR_OUT_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary format.

</td>
</tr>
</table>
 


### -param pstrCRL






#### - pbstrCRL [out]

A pointer to a <b>BSTR</b> that receives the CRL.

When using this method, create a variable of <b>BSTR</b> type, set the variable to <b>NULL</b>, and pass the address of this variable in the <i>pbstrCRL</i> parameter. When you have finished using the <b>BSTR</b> variable, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.


## -returns



If the function succeeds, the function returns S_OK.



If the function fails, it returns an HRESULT value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>strConfig</i> parameter cannot be <b>NULL</b> or no CRL has been found.

</td>
</tr>
</table>
 




## -remarks



Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.


#### Examples

The following example declares the necessary variables, initializes COM, and creates an instance of the <b>CertAdmin</b> class. It then calls <b>GetCRL</b> and prints success or failure to the screen. Finally, it frees resources.


<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    ICertAdmin * pCertAdmin = NULL;  // pointer to interface object
    BSTR bstrCA = NULL;              // variable for machine\CAName
    BSTR bstrCRL = NULL;             // variable to contain
                                     // the retrieved CRL

    HRESULT hr;

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (FAILED(hr))
    {
        printf("Failed CoInitializeEx [%x]\n", hr);
        goto error;
    }

    //  Create the CertAdmin object
    //  and get a pointer to its ICertAdmin interface.
    hr = CoCreateInstance( CLSID_CCertAdmin,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ICertAdmin,
                           (void **)&amp;pCertAdmin);
    if (FAILED(hr))
    {
        printf("Failed CoCreateInstance pCertAdmin [%x]\n", hr);
        goto error;
    }

    //  Note the use of two backslashes (\\) 
   //  in C++ to produce one backslash (\).
    bstrCA = SysAllocString(L"&lt;COMPUTERNAMEHERE&gt;\\&lt;CANAMEHERE&gt;");
    if (FAILED(hr))
    {
        printf("Failed to allocate memory for bstrCA\n");
        goto error;
    }

    //  Retrieve the CRL.
    hr = pCertAdmin-&gt;GetCRL( bstrCA, CR_OUT_BINARY, &amp;bstrCRL );
    if (FAILED(hr))
    {
        printf("Failed GetCRL [%x]\n", hr);
        goto error;
    }
    else
        printf("CRL retrieved successfully\n");
        //  Use the CRL as needed.

    //  Done processing.

error:

    //  Free BSTR values.
    if (NULL != bstrCA)
        SysFreeString(bstrCA);

    if (NULL != bstrCRL)
        SysFreeString(bstrCRL);

    //  Clean up object resources.
    if (NULL != pCertAdmin)
        pCertAdmin-&gt;Release();

    //  Free COM resources.
    CoUninitialize();
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">CCertAdmin</a>



<a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a>



<b>ICertAdmin2</b>



<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>
 

 

