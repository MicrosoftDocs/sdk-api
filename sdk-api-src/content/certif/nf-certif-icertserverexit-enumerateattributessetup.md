---
UID: NF:certif.ICertServerExit.EnumerateAttributesSetup
title: ICertServerExit::EnumerateAttributesSetup (certif.h)
description: Initializes the internal enumeration pointer to the first request attribute associated with the current context. (ICertServerExit.EnumerateAttributesSetup)
helpviewer_keywords: ["CCertServerExit object [Security]","EnumerateAttributesSetup method","EnumerateAttributesSetup","EnumerateAttributesSetup method [Security]","EnumerateAttributesSetup method [Security]","CCertServerExit object","EnumerateAttributesSetup method [Security]","ICertServerExit interface","ICertServerExit interface [Security]","EnumerateAttributesSetup method","ICertServerExit.EnumerateAttributesSetup","ICertServerExit::EnumerateAttributesSetup","_certsrv_icertserverexit_enumerateattributessetup","certif/ICertServerExit::EnumerateAttributesSetup","security.icertserverexit_enumerateattributessetup"]
old-location: security\icertserverexit_enumerateattributessetup.htm
tech.root: security
ms.assetid: c81b9c4d-483e-48b8-a270-f570e148d371
ms.date: 12/05/2018
ms.keywords: CCertServerExit object [Security],EnumerateAttributesSetup method, EnumerateAttributesSetup, EnumerateAttributesSetup method [Security], EnumerateAttributesSetup method [Security],CCertServerExit object, EnumerateAttributesSetup method [Security],ICertServerExit interface, ICertServerExit interface [Security],EnumerateAttributesSetup method, ICertServerExit.EnumerateAttributesSetup, ICertServerExit::EnumerateAttributesSetup, _certsrv_icertserverexit_enumerateattributessetup, certif/ICertServerExit::EnumerateAttributesSetup, security.icertserverexit_enumerateattributessetup
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
 - ICertServerExit::EnumerateAttributesSetup
 - certif/ICertServerExit::EnumerateAttributesSetup
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
 - ICertServerExit.EnumerateAttributesSetup
 - CCertServerExit.EnumerateAttributesSetup
---

# ICertServerExit::EnumerateAttributesSetup


## -description

The <b>EnumerateAttributesSetup</b> method initializes the internal enumeration pointer to the first request attribute associated with the current context.

## -parameters

### -param Flags [in]

This parameter is reserved and must be set to zero.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

You must call 
<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-setcontext">ICertServerExit::SetContext</a> prior to using this method.


#### Examples


```cpp
// Set up the enumeration.
hr = pCertServerExit->EnumerateAttributesSetup(0);
if (FAILED(hr))
{
    printf("Failed EnumerateAttributesSetup [%x]\n", hr);
    goto error;
}
```

## -see-also

<a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-enumerateattributes">ICertServerExit::EnumerateAttributes</a>
