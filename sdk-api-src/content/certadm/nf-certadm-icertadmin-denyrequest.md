---
UID: NF:certadm.ICertAdmin.DenyRequest
title: ICertAdmin::DenyRequest
author: windows-sdk-content
description: Denies a specified certificate request that is pending.
old-location: security\icertadmin2_denyrequest.htm
tech.root: seccrypto
ms.assetid: a432fd66-0f80-4fb8-9778-38b240dd6369
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: CCertAdmin interface [Security],DenyRequest method, DenyRequest, DenyRequest method [Security], DenyRequest method [Security],CCertAdmin interface, DenyRequest method [Security],ICertAdmin interface, DenyRequest method [Security],ICertAdmin2 interface, ICertAdmin interface [Security],DenyRequest method, ICertAdmin.DenyRequest, ICertAdmin2 interface [Security],DenyRequest method, ICertAdmin2::DenyRequest, ICertAdmin::DenyRequest, certadm/ICertAdmin2::DenyRequest, certadm/ICertAdmin::DenyRequest, security.icertadmin2_denyrequest
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.DenyRequest
 - ICertAdmin.DenyRequest
 - CCertAdmin.DenyRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertAdmin::DenyRequest


## -description


The <b>DenyRequest</b> method denies a specified <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a> that is pending. This method was first defined in the <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a> interface.

For this method to succeed, the certificate request must be pending.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) in the form COMPUTERNAME\CANAME where COMPUTERNAME is the network name of the Certificate Services server and CANAME is the common name of the certification authority as entered during Certificate Services setup. For information about the configuration string, see <a href="https://msdn.microsoft.com/en-us/library/Aa383268(v=VS.85).aspx">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>DenyRequest</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="https://msdn.microsoft.com/en-us/library/Aa383234(v=VS.85).aspx">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param RequestId [in]

Specifies the ID of the pending request to be denied.


## -remarks



Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.


#### Examples

The following example declares the necessary variables, initializes COM, and creates an instance of the CertAdmin class. It then calls DenyRequest and prints success or failure to the screen. Finally, it frees resources.



<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//  Pointer to an interface object.
ICertAdmin * pCertAdmin = NULL;

    BSTR       bstrCA = NULL;  // variable for machine\CAName
    long       nReqID;         // variable for Request ID
    HRESULT    hr;

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

    //  Note the use of two '\' in C++ to produce one '\'.
    bstrCA = SysAllocString(L"&lt;COMPUTERNAMEHERE&gt;\\&lt;CANAMEHERE&gt;");
    if (NULL == bstrCA)
    {
        printf("Failed to allocate memory for bstrCA\n");
        goto error;
    }

    //  nReqID is RequestID to be denied.
    nReqID = &lt;REQUESTIDHERE&gt;;

    //  Deny the request.
    hr = pCertAdmin-&gt;DenyRequest( bstrCA, nReqID );
    if (FAILED(hr))
    {
        printf("Failed DenyRequest %ws %d [%x]\n",
               bstrCA, nReqID, hr);
        goto error;
    }
    else
        printf("Denied request %ws %d\n",
                bstrCA, nReqID );

    //  Done processing.

    
error:

    //  Free BSTR values.
    if (NULL != bstrCA)
        SysFreeString(bstrCA);

    //  Clean up object resources.
    if (NULL != pCertAdmin)
        pCertAdmin-&gt;Release();

    //  Free COM resources.
    CoUninitialize(); </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383234(v=VS.85).aspx">CCertAdmin</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a>



<b>ICertAdmin2</b>



<a href="https://msdn.microsoft.com/en-us/library/Aa383268(v=VS.85).aspx">ICertConfig</a>
 

 

