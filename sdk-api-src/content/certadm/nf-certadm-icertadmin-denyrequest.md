---
UID: NF:certadm.ICertAdmin.DenyRequest
title: ICertAdmin::DenyRequest (certadm.h)
description: Denies a specified certificate request that is pending.
helpviewer_keywords: ["CCertAdmin interface [Security]","DenyRequest method","DenyRequest","DenyRequest method [Security]","DenyRequest method [Security]","CCertAdmin interface","DenyRequest method [Security]","ICertAdmin interface","DenyRequest method [Security]","ICertAdmin2 interface","ICertAdmin interface [Security]","DenyRequest method","ICertAdmin.DenyRequest","ICertAdmin2 interface [Security]","DenyRequest method","ICertAdmin2::DenyRequest","ICertAdmin::DenyRequest","certadm/ICertAdmin2::DenyRequest","certadm/ICertAdmin::DenyRequest","security.icertadmin2_denyrequest"]
old-location: security\icertadmin2_denyrequest.htm
tech.root: security
ms.assetid: a432fd66-0f80-4fb8-9778-38b240dd6369
ms.date: 12/05/2018
ms.keywords: CCertAdmin interface [Security],DenyRequest method, DenyRequest, DenyRequest method [Security], DenyRequest method [Security],CCertAdmin interface, DenyRequest method [Security],ICertAdmin interface, DenyRequest method [Security],ICertAdmin2 interface, ICertAdmin interface [Security],DenyRequest method, ICertAdmin.DenyRequest, ICertAdmin2 interface [Security],DenyRequest method, ICertAdmin2::DenyRequest, ICertAdmin::DenyRequest, certadm/ICertAdmin2::DenyRequest, certadm/ICertAdmin::DenyRequest, security.icertadmin2_denyrequest
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
 - ICertAdmin::DenyRequest
 - certadm/ICertAdmin::DenyRequest
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
 - ICertAdmin2.DenyRequest
 - ICertAdmin.DenyRequest
 - CCertAdmin.DenyRequest
---

# ICertAdmin::DenyRequest


## -description

The <b>DenyRequest</b> method denies a specified <a href="/windows/desktop/SecGloss/c-gly">certificate request</a> that is pending. This method was first defined in the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> interface.

For this method to succeed, the certificate request must be pending.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) in the form COMPUTERNAME\CANAME where COMPUTERNAME is the network name of the Certificate Services server and CANAME is the common name of the certification authority as entered during Certificate Services setup. For information about the configuration string, see <a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>DenyRequest</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param RequestId [in]

Specifies the ID of the pending request to be denied.

## -remarks

Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.


#### Examples

The following example declares the necessary variables, initializes COM, and creates an instance of the CertAdmin class. It then calls DenyRequest and prints success or failure to the screen. Finally, it frees resources.




```cpp
//  Pointer to an interface object.
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
                           (void **)&pCertAdmin);
    if (FAILED(hr))
    {
        printf("Failed CoCreateInstance pCertAdmin [%x]\n", hr);
        goto error;
    }

    //  Note the use of two '\' in C++ to produce one '\'.
    bstrCA = SysAllocString(L"<COMPUTERNAMEHERE>\\<CANAMEHERE>");
    if (NULL == bstrCA)
    {
        printf("Failed to allocate memory for bstrCA\n");
        goto error;
    }

    //  nReqID is RequestID to be denied.
    nReqID = <REQUESTIDHERE>;

    //  Deny the request.
    hr = pCertAdmin->DenyRequest( bstrCA, nReqID );
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
        pCertAdmin->Release();

    //  Free COM resources.
    CoUninitialize(); 
```

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">CCertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a>



<b>ICertAdmin2</b>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>