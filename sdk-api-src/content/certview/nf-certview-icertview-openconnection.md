---
UID: NF:certview.ICertView.OpenConnection
title: ICertView::OpenConnection (certview.h)
description: Establishes a connection with a Certificate Services server.
helpviewer_keywords: ["CCertView object [Security]","OpenConnection method","ICertView interface [Security]","OpenConnection method","ICertView.OpenConnection","ICertView2 interface [Security]","OpenConnection method","ICertView2::OpenConnection","ICertView::OpenConnection","OpenConnection","OpenConnection method [Security]","OpenConnection method [Security]","CCertView object","OpenConnection method [Security]","ICertView interface","OpenConnection method [Security]","ICertView2 interface","certview/ICertView2::OpenConnection","certview/ICertView::OpenConnection","security.icertview2_openconnection"]
old-location: security\icertview2_openconnection.htm
tech.root: security
ms.assetid: 576af4d1-88c9-40e3-9438-9fefd483be7a
ms.date: 12/05/2018
ms.keywords: CCertView object [Security],OpenConnection method, ICertView interface [Security],OpenConnection method, ICertView.OpenConnection, ICertView2 interface [Security],OpenConnection method, ICertView2::OpenConnection, ICertView::OpenConnection, OpenConnection, OpenConnection method [Security], OpenConnection method [Security],CCertView object, OpenConnection method [Security],ICertView interface, OpenConnection method [Security],ICertView2 interface, certview/ICertView2::OpenConnection, certview/ICertView::OpenConnection, security.icertview2_openconnection
req.header: certview.h
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
 - ICertView::OpenConnection
 - certview/ICertView::OpenConnection
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
 - ICertView2.OpenConnection
 - ICertView.OpenConnection
 - CCertView.OpenConnection
---

# ICertView::OpenConnection


## -description

The <b>OpenConnection</b> method establishes a connection with a Certificate Services server.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the Certificate Services server. The configuration string is in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the server's network name, and CANAME is the common name of the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Upon successful completion of this method, the 
<a href="/windows/desktop/api/certview/nn-certview-icertview">ICertView</a> object will have a connection to the Certificate Services server specified in the  <i>strConfig</i> parameter.

 To close the connection, call the <b>Release</b> function.


#### Examples


```cpp
ICertView *   pCertView = NULL;
BSTR          strCertServ = NULL;
HRESULT       hr;

// Initialize COM.
hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

if (FAILED(hr))
{
    printf("Failed CoInitializeEx\n");
    goto error;
}
// Get pointer to the ICertView interface.
hr = CoCreateInstance(CLSID_CCertView,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_ICertView,
                      (void **)&pCertView);
if (FAILED(hr))
{
    printf("Failed CoCreateInstance\n");
    goto error;
}
// The use of '\\' is necessary to represent a single backslash.
strCertServ = SysAllocString(TEXT("Server01\\ABCCertServ"));
// Open the connection to the Certificate Services server.
hr = pCertView->OpenConnection(strCertServ);
if (FAILED(hr))
{
    printf("Failed OpenConnection!\n");
    goto error;
}
else
    // Established successful connection; use view as appropriate.
    // ...
    // Done using objects; free resources.
error: 
    if (NULL != pCertView)
        pCertView->Release();
    if (NULL != strCertServ)
        SysFreeString(strCertServ);
    // Free COM resources.
    CoUninitialize();
```

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certview/nn-certview-icertview">ICertView</a>



<a href="/windows/desktop/api/certview/nn-certview-icertview2">ICertView2</a>



<a href="/windows/desktop/api/certview/nf-certview-icertview-openview">ICertView::OpenView</a>