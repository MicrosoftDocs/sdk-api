---
UID: NF:certif.ICertServerPolicy.EnumerateAttributesSetup
title: ICertServerPolicy::EnumerateAttributesSetup (certif.h)
description: Initializes the internal enumeration pointer to the first request attribute associated with the current context. (ICertServerPolicy.EnumerateAttributesSetup)
helpviewer_keywords: ["CCertServerPolicy object [Security]","EnumerateAttributesSetup method","EnumerateAttributesSetup","EnumerateAttributesSetup method [Security]","EnumerateAttributesSetup method [Security]","CCertServerPolicy object","EnumerateAttributesSetup method [Security]","ICertServerPolicy interface","ICertServerPolicy interface [Security]","EnumerateAttributesSetup method","ICertServerPolicy.EnumerateAttributesSetup","ICertServerPolicy::EnumerateAttributesSetup","_certsrv_icertserverpolicy_enumerateattributessetup","certif/ICertServerPolicy::EnumerateAttributesSetup","security.icertserverpolicy_enumerateattributessetup"]
old-location: security\icertserverpolicy_enumerateattributessetup.htm
tech.root: security
ms.assetid: 14b81b88-36db-4b01-96e6-eafed22ae02e
ms.date: 12/05/2018
ms.keywords: CCertServerPolicy object [Security],EnumerateAttributesSetup method, EnumerateAttributesSetup, EnumerateAttributesSetup method [Security], EnumerateAttributesSetup method [Security],CCertServerPolicy object, EnumerateAttributesSetup method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],EnumerateAttributesSetup method, ICertServerPolicy.EnumerateAttributesSetup, ICertServerPolicy::EnumerateAttributesSetup, _certsrv_icertserverpolicy_enumerateattributessetup, certif/ICertServerPolicy::EnumerateAttributesSetup, security.icertserverpolicy_enumerateattributessetup
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
 - ICertServerPolicy::EnumerateAttributesSetup
 - certif/ICertServerPolicy::EnumerateAttributesSetup
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
 - ICertServerPolicy.EnumerateAttributesSetup
 - CCertServerPolicy.EnumerateAttributesSetup
---

# ICertServerPolicy::EnumerateAttributesSetup


## -description

The <b>EnumerateAttributesSetup</b> method initializes the internal enumeration pointer to the first request  <a href="/windows/desktop/SecGloss/a-gly">attribute</a> associated with the current <a href="/windows/desktop/SecGloss/c-gly">context</a>.

## -parameters

### -param Flags [in]

This parameter is reserved and must be set to zero.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The 
<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">SetContext</a> method must be called prior to calling this method. The call to <b>SetContext</b> specifies which request to use as the current context.

To retrieve the attribute, call the <a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateattributes">EnumerateAttributes</a> method. The call to <b>EnumerateAttributes</b> retrieves the first attribute and moves the index to the next attribute if one exists.


#### Examples


```cpp
// Set the context. The value nContext (long) would be the same
// as the context parameter in ICertPolicy::VerifyRequest.
// hr is defined as an HRESULT.
// pCertServerPolicy has been used to call SetContext previously.
hr = pCertServerPolicy->SetContext(nContext);
if (FAILED(hr))
{
    printf("Failed SetContext [%x]\n", hr);
    goto error;
}

// Setup the enumeration.
hr = pCertServerPolicy->EnumerateAttributesSetup(0);
if (FAILED(hr))
{
    printf("Failed EnumerateAttributesSetup [%x]\n", hr);
    goto error;
}
```

## -see-also

<a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateattributes">ICertServerPolicy::EnumerateAttributes</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateattributesclose">ICertServerPolicy::EnumerateAttributesClose</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">ICertServerPolicy::SetContext</a>
