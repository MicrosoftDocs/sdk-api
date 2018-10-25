---
UID: NF:certif.ICertServerExit.EnumerateExtensionsSetup
title: ICertServerExit::EnumerateExtensionsSetup
author: windows-sdk-content
description: Initializes the internal enumeration pointer to the first certificate extension associated with the current context.
old-location: security\icertserverexit_enumerateextensionssetup.htm
tech.root: seccrypto
ms.assetid: 2a0c4919-b3a0-4027-85bd-970f6bc0cdeb
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CCertServerExit object [Security],EnumerateExtensionsSetup method, EnumerateExtensionsSetup, EnumerateExtensionsSetup method [Security], EnumerateExtensionsSetup method [Security],CCertServerExit object, EnumerateExtensionsSetup method [Security],ICertServerExit interface, ICertServerExit interface [Security],EnumerateExtensionsSetup method, ICertServerExit.EnumerateExtensionsSetup, ICertServerExit::EnumerateExtensionsSetup, _certsrv_icertserverexit_enumerateextensionssetup, certif/ICertServerExit::EnumerateExtensionsSetup, security.icertserverexit_enumerateextensionssetup
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
 - ICertServerExit.EnumerateExtensionsSetup
 - CCertServerExit.EnumerateExtensionsSetup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertServerExit::EnumerateExtensionsSetup


## -description


The <b>EnumerateExtensionsSetup</b> method initializes the internal enumeration pointer to the first certificate extension associated with the current context.

The enumeration process enumerates certificate extensions recorded in the database, even those that are disabled and do not appear in the certificate.


## -parameters




### -param Flags [in]

This parameter is reserved and must be set to zero.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



You must call 
<a href="https://msdn.microsoft.com/8d317114-17bd-4b22-8e37-99db72740538">ICertServerExit::SetContext</a> before using this method.


#### Examples


```cpp
// Set the context. The value nContext (long) would be the same
// as the context parameter in ICertExit::Notify.
// hr is defined as an HRESULT.
hr = pCertServerExit->SetContext( nContext );
if (FAILED(hr))
{
    printf("Failed SetContext [%x]\n", hr);
    goto error;
}

// Setup the enumeration.
hr = pCertServerExit->EnumerateExtensionsSetup( 0 );
if (FAILED(hr))
{
    printf("Failed EnumerateExtensionsSetup [%x]\n", hr);
    goto error;
}
```





## -see-also




<a href="https://msdn.microsoft.com/1554c09c-a7c1-44ad-9821-93c0913212fc">ICertServerExit</a>



<a href="https://msdn.microsoft.com/8726f5fa-dc85-4357-b73a-013842d6ab78">ICertServerExit::EnumerateExtensions</a>



<a href="https://msdn.microsoft.com/769235cd-d5ef-458b-a04b-88f9f831ce3f">ICertServerExit::EnumerateExtensionsClose</a>
 

 

