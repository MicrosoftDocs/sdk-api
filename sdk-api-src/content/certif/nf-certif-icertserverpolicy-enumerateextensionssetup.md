---
UID: NF:certif.ICertServerPolicy.EnumerateExtensionsSetup
title: ICertServerPolicy::EnumerateExtensionsSetup (certif.h)
description: Initializes the internal enumeration pointer to the first certificate extension associated with the current context. (ICertServerPolicy.EnumerateExtensionsSetup)
helpviewer_keywords: ["CCertServerPolicy object [Security]","EnumerateExtensionsSetup method","EnumerateExtensionsSetup","EnumerateExtensionsSetup method [Security]","EnumerateExtensionsSetup method [Security]","CCertServerPolicy object","EnumerateExtensionsSetup method [Security]","ICertServerPolicy interface","ICertServerPolicy interface [Security]","EnumerateExtensionsSetup method","ICertServerPolicy.EnumerateExtensionsSetup","ICertServerPolicy::EnumerateExtensionsSetup","_certsrv_icertserverpolicy_enumerateextensionssetup","certif/ICertServerPolicy::EnumerateExtensionsSetup","security.icertserverpolicy_enumerateextensionssetup"]
old-location: security\icertserverpolicy_enumerateextensionssetup.htm
tech.root: security
ms.assetid: e7ad32a5-d7df-407f-8efe-c9931610c2d2
ms.date: 12/05/2018
ms.keywords: CCertServerPolicy object [Security],EnumerateExtensionsSetup method, EnumerateExtensionsSetup, EnumerateExtensionsSetup method [Security], EnumerateExtensionsSetup method [Security],CCertServerPolicy object, EnumerateExtensionsSetup method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],EnumerateExtensionsSetup method, ICertServerPolicy.EnumerateExtensionsSetup, ICertServerPolicy::EnumerateExtensionsSetup, _certsrv_icertserverpolicy_enumerateextensionssetup, certif/ICertServerPolicy::EnumerateExtensionsSetup, security.icertserverpolicy_enumerateextensionssetup
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
 - ICertServerPolicy::EnumerateExtensionsSetup
 - certif/ICertServerPolicy::EnumerateExtensionsSetup
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
 - ICertServerPolicy.EnumerateExtensionsSetup
 - CCertServerPolicy.EnumerateExtensionsSetup
---

# ICertServerPolicy::EnumerateExtensionsSetup


## -description

The <b>EnumerateExtensionsSetup</b> method initializes the internal enumeration pointer to the first certificate extension associated with the current context.

## -parameters

### -param Flags [in]

This parameter is reserved and must be set to zero.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The 
<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">SetContext</a> method must be called prior to calling this method. The call to <b>SetContext</b> specifies which request is the current context.

To retrieve the extension, call the <a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateextensions">EnumerateExtensions</a> method. The call to <b>EnumerateExtensions</b> retrieves the first extension and moves the index to the next extension if one exists.


#### Examples


```cpp
// Set the context. The value nContext (long) would be the same
// as the context parameter in ICertPolicy::VerifyRequest.
// hr is defined as an HRESULT.
// pCertServerPolicy has been used to call SetContext previously.
hr = pCertServerPolicy->SetContext( nContext );
if (FAILED(hr))
{
    printf("Failed SetContext [%x]\n", hr);
    goto error;
}
// Setup the enumeration.
hr = pCertServerPolicy->EnumerateExtensionsSetup( 0 );
if (FAILED(hr))
{
    printf("Failed EnumerateExtensionsSetup [%x]\n", hr);
    goto error;
}
```

## -see-also

<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateextensions">EnumerateExtensions</a>



<a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">SetContext</a>
