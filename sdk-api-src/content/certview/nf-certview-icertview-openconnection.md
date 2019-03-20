---
UID: NF:certview.ICertView.OpenConnection
title: ICertView::OpenConnection (certview.h)
author: windows-sdk-content
description: Establishes a connection with a Certificate Services server.
old-location: security\icertview2_openconnection.htm
tech.root: SecCrypto
ms.assetid: 576af4d1-88c9-40e3-9438-9fefd483be7a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCertView object [Security],OpenConnection method, ICertView interface [Security],OpenConnection method, ICertView.OpenConnection, ICertView2 interface [Security],OpenConnection method, ICertView2::OpenConnection, ICertView::OpenConnection, OpenConnection, OpenConnection method [Security], OpenConnection method [Security],CCertView object, OpenConnection method [Security],ICertView interface, OpenConnection method [Security],ICertView2 interface, certview/ICertView2::OpenConnection, certview/ICertView::OpenConnection, security.icertview2_openconnection
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertView::OpenConnection


## -description


The <b>OpenConnection</b> method establishes a connection with a Certificate Services server.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the Certificate Services server. The configuration string is in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the server's network name, and CANAME is the common name of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Upon successful completion of this method, the 
<a href="https://msdn.microsoft.com/0b6660ee-458f-457f-8a38-0d950aee2710">ICertView</a> object will have a connection to the Certificate Services server specified in the  <i>strConfig</i> parameter.

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




<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>



<a href="https://msdn.microsoft.com/0b6660ee-458f-457f-8a38-0d950aee2710">ICertView</a>



<a href="https://msdn.microsoft.com/c29f1db3-0cdf-463e-a202-47fbba8e1c81">ICertView2</a>



<a href="https://msdn.microsoft.com/d68a5463-f711-4737-b0ad-889f7e4855d5">ICertView::OpenView</a>
 

 

