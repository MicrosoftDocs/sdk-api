---
UID: NF:certif.ICertServerPolicy.SetContext
title: ICertServerPolicy::SetContext (certif.h)
description: Specifies the request to be used as the context for subsequent calls to Certificate Services.
helpviewer_keywords: ["CCertServerPolicy object [Security]","SetContext method","ICertServerPolicy interface [Security]","SetContext method","ICertServerPolicy.SetContext","ICertServerPolicy::SetContext","SetContext","SetContext method [Security]","SetContext method [Security]","CCertServerPolicy object","SetContext method [Security]","ICertServerPolicy interface","_certsrv_icertserverpolicy_setcontext","certif/ICertServerPolicy::SetContext","security.icertserverpolicy_setcontext"]
old-location: security\icertserverpolicy_setcontext.htm
tech.root: security
ms.assetid: ba45cda8-49a5-4bd6-af68-90b4b56aff7d
ms.date: 12/05/2018
ms.keywords: CCertServerPolicy object [Security],SetContext method, ICertServerPolicy interface [Security],SetContext method, ICertServerPolicy.SetContext, ICertServerPolicy::SetContext, SetContext, SetContext method [Security], SetContext method [Security],CCertServerPolicy object, SetContext method [Security],ICertServerPolicy interface, _certsrv_icertserverpolicy_setcontext, certif/ICertServerPolicy::SetContext, security.icertserverpolicy_setcontext
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
 - ICertServerPolicy::SetContext
 - certif/ICertServerPolicy::SetContext
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
 - ICertServerPolicy.SetContext
 - CCertServerPolicy.SetContext
---

# ICertServerPolicy::SetContext


## -description

The <b>SetContext</b> method specifies the request  to be used as the <a href="/windows/desktop/SecGloss/c-gly">context</a> for subsequent calls to Certificate Services.

## -parameters

### -param Context [in]

Specifies the request. This  parameter must be set to the identical value returned in the  <i>Context</i> parameter of the  
<a href="/windows/desktop/api/certpol/nf-certpol-icertpolicy-verifyrequest">ICertPolicy::VerifyRequest</a> method.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The policy module must call the <b>SetContext</b> method first, before calls to any other <a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a> method,  so that the interface  references a valid request.


#### Examples


```cpp
// Set the context. The value nContext (long) would be the same
// as the context parameter in ICertPolicy::VerifyRequest.
// hr is defined as an HRESULT.
hr = pCertServerPolicy->SetContext( nContext );
if (FAILED(hr))
{
    printf("Failed SetContext [%x]\n", hr);
    goto error;
}
```

## -see-also

<a href="/windows/desktop/api/certpol/nf-certpol-icertpolicy-verifyrequest">ICertPolicy::VerifyRequest</a>



<a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a>