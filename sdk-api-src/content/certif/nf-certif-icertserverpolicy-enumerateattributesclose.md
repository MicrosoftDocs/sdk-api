---
UID: NF:certif.ICertServerPolicy.EnumerateAttributesClose
title: ICertServerPolicy::EnumerateAttributesClose (certif.h)
description: Frees the resources connected with attribute enumeration.
helpviewer_keywords: ["CCertServerPolicy object [Security]","EnumerateAttributesClose method","EnumerateAttributesClose","EnumerateAttributesClose method [Security]","EnumerateAttributesClose method [Security]","CCertServerPolicy object","EnumerateAttributesClose method [Security]","ICertServerPolicy interface","ICertServerPolicy interface [Security]","EnumerateAttributesClose method","ICertServerPolicy.EnumerateAttributesClose","ICertServerPolicy::EnumerateAttributesClose","_certsrv_icertserverpolicy_enumerateattributesclose","certif/ICertServerPolicy::EnumerateAttributesClose","security.icertserverpolicy_enumerateattributesclose"]
old-location: security\icertserverpolicy_enumerateattributesclose.htm
tech.root: security
ms.assetid: 91cb8edd-7735-44c5-b2c5-d46fa1e33e41
ms.date: 12/05/2018
ms.keywords: CCertServerPolicy object [Security],EnumerateAttributesClose method, EnumerateAttributesClose, EnumerateAttributesClose method [Security], EnumerateAttributesClose method [Security],CCertServerPolicy object, EnumerateAttributesClose method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],EnumerateAttributesClose method, ICertServerPolicy.EnumerateAttributesClose, ICertServerPolicy::EnumerateAttributesClose, _certsrv_icertserverpolicy_enumerateattributesclose, certif/ICertServerPolicy::EnumerateAttributesClose, security.icertserverpolicy_enumerateattributesclose
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
 - ICertServerPolicy::EnumerateAttributesClose
 - certif/ICertServerPolicy::EnumerateAttributesClose
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
 - ICertServerPolicy.EnumerateAttributesClose
 - CCertServerPolicy.EnumerateAttributesClose
---

# ICertServerPolicy::EnumerateAttributesClose


## -description

The <b>EnumerateAttributesClose</b> method frees the resources connected with attribute enumeration.



## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

All policy modules should call the <b>EnumerateAttributesClose</b> method after calling the <a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateattributessetup">EnumerateAttributesSetup</a> and  
<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateattributes">EnumerateAttributes</a> methods.


#### Examples


```cpp
// Close the enumeration.
// hr is defined as an HRESULT.
hr = pCertServerPolicy->EnumerateAttributesClose();
if (FAILED(hr))
{
    printf("Failed EnumerateAttributesClose [%x]\n", hr);
    goto error;
}
```

## -see-also

<a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateattributes">ICertServerPolicy::EnumerateAttributes</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-enumerateattributessetup">ICertServerPolicy::EnumerateAttributesSetup</a>
