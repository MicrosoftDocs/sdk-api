---
UID: NF:certif.ICertServerExit.EnumerateExtensionsSetup
title: ICertServerExit::EnumerateExtensionsSetup (certif.h)
description: Initializes the internal enumeration pointer to the first certificate extension associated with the current context. (ICertServerExit.EnumerateExtensionsSetup)
helpviewer_keywords: ["CCertServerExit object [Security]","EnumerateExtensionsSetup method","EnumerateExtensionsSetup","EnumerateExtensionsSetup method [Security]","EnumerateExtensionsSetup method [Security]","CCertServerExit object","EnumerateExtensionsSetup method [Security]","ICertServerExit interface","ICertServerExit interface [Security]","EnumerateExtensionsSetup method","ICertServerExit.EnumerateExtensionsSetup","ICertServerExit::EnumerateExtensionsSetup","_certsrv_icertserverexit_enumerateextensionssetup","certif/ICertServerExit::EnumerateExtensionsSetup","security.icertserverexit_enumerateextensionssetup"]
old-location: security\icertserverexit_enumerateextensionssetup.htm
tech.root: security
ms.assetid: 2a0c4919-b3a0-4027-85bd-970f6bc0cdeb
ms.date: 12/05/2018
ms.keywords: CCertServerExit object [Security],EnumerateExtensionsSetup method, EnumerateExtensionsSetup, EnumerateExtensionsSetup method [Security], EnumerateExtensionsSetup method [Security],CCertServerExit object, EnumerateExtensionsSetup method [Security],ICertServerExit interface, ICertServerExit interface [Security],EnumerateExtensionsSetup method, ICertServerExit.EnumerateExtensionsSetup, ICertServerExit::EnumerateExtensionsSetup, _certsrv_icertserverexit_enumerateextensionssetup, certif/ICertServerExit::EnumerateExtensionsSetup, security.icertserverexit_enumerateextensionssetup
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertServerExit::EnumerateExtensionsSetup
 - certif/ICertServerExit::EnumerateExtensionsSetup
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
 - ICertServerExit.EnumerateExtensionsSetup
 - CCertServerExit.EnumerateExtensionsSetup
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

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

You must call 
<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-setcontext">ICertServerExit::SetContext</a> before using this method.


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

<a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateextensions">ICertServerExit::EnumerateExtensions</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateextensionsclose">ICertServerExit::EnumerateExtensionsClose</a>
