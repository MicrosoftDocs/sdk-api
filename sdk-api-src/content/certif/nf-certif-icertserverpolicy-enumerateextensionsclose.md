---
UID: NF:certif.ICertServerPolicy.EnumerateExtensionsClose
title: ICertServerPolicy::EnumerateExtensionsClose
author: windows-sdk-content
description: Frees the resources connected with extension enumeration.
old-location: security\icertserverpolicy_enumerateextensionsclose.htm
tech.root: seccrypto
ms.assetid: b1755fc5-f18f-45b5-a89a-44c6598c0e2c
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CCertServerPolicy object [Security],EnumerateExtensionsClose method, EnumerateExtensionsClose, EnumerateExtensionsClose method [Security], EnumerateExtensionsClose method [Security],CCertServerPolicy object, EnumerateExtensionsClose method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],EnumerateExtensionsClose method, ICertServerPolicy.EnumerateExtensionsClose, ICertServerPolicy::EnumerateExtensionsClose, _certsrv_icertserverpolicy_enumerateextensionsclose, certif/ICertServerPolicy::EnumerateExtensionsClose, security.icertserverpolicy_enumerateextensionsclose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertServerPolicy.EnumerateExtensionsClose
 - CCertServerPolicy.EnumerateExtensionsClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertServerPolicy::EnumerateExtensionsClose


## -description


The <b>EnumerateExtensionsClose</b> method frees the resources connected with extension enumeration.


## -parameters






## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



All policy modules should call the <b>EnumerateExtensionsClose</b> method after calling the <a href="https://msdn.microsoft.com/en-us/library/Aa385086(v=VS.85).aspx">EnumerateExtensionsSetup</a> and 
<a href="https://msdn.microsoft.com/en-us/library/Aa385084(v=VS.85).aspx">ICertServerPolicy::EnumerateExtensions</a> methods.


#### Examples


```cpp
// Close the enumeration.
// hr is defined as an HRESULT.
hr = pCertServerPolicy->EnumerateExtensionsClose();
if (FAILED(hr))
{
    printf("Failed EnumerateExtensionsClose [%x]\n", hr);
    goto error;
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385066(v=VS.85).aspx">ICertServerExit::EnumerateExtensionsSetup</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385080(v=VS.85).aspx">ICertServerPolicy</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385084(v=VS.85).aspx">ICertServerPolicy::EnumerateExtensions</a>
 

 

