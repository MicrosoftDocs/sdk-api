---
UID: NF:certpol.ICertPolicy.ShutDown
title: ICertPolicy::ShutDown (certpol.h)
description: Called by the server engine before the server is terminated.
helpviewer_keywords: ["CCertPolicy object [Security]","ShutDown method","ICertPolicy interface [Security]","ShutDown method","ICertPolicy.ShutDown","ICertPolicy2 interface [Security]","ShutDown method","ICertPolicy2::ShutDown","ICertPolicy::ShutDown","ShutDown","ShutDown method [Security]","ShutDown method [Security]","CCertPolicy object","ShutDown method [Security]","ICertPolicy interface","ShutDown method [Security]","ICertPolicy2 interface","_certsrv_icertpolicy_shutdown","certpol/ICertPolicy2::ShutDown","certpol/ICertPolicy::ShutDown","security.icertpolicy2_shutdown"]
old-location: security\icertpolicy2_shutdown.htm
tech.root: security
ms.assetid: 2a796acb-b179-4b6f-8864-9e96f4049389
ms.date: 12/05/2018
ms.keywords: CCertPolicy object [Security],ShutDown method, ICertPolicy interface [Security],ShutDown method, ICertPolicy.ShutDown, ICertPolicy2 interface [Security],ShutDown method, ICertPolicy2::ShutDown, ICertPolicy::ShutDown, ShutDown, ShutDown method [Security], ShutDown method [Security],CCertPolicy object, ShutDown method [Security],ICertPolicy interface, ShutDown method [Security],ICertPolicy2 interface, _certsrv_icertpolicy_shutdown, certpol/ICertPolicy2::ShutDown, certpol/ICertPolicy::ShutDown, security.icertpolicy2_shutdown
req.header: certpol.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertPolicy::ShutDown
 - certpol/ICertPolicy::ShutDown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certidl.lib
 - Certidl.dll
api_name:
 - ICertPolicy2.ShutDown
 - ICertPolicy.ShutDown
 - CCertPolicy.ShutDown
---

# ICertPolicy::ShutDown


## -description

The <b>ShutDown</b> method is called by the server engine before the server is terminated.

When <b>ShutDown</b> is called, the policy module should clean up and stop. It is guaranteed that no requests will arrive after <b>ShutDown</b> is called.



## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

When you write custom policy modules, implement this method.


#### Examples


```cpp
#include <windows.h>
#include <stdio.h>
#include <Certpol.h>

STDMETHODIMP CCertPolicy::ShutDown()
{
    // Clean up resources used by this process.

    // Display message that this method has been called.
    if ( fDebug )
    {
        printf("Policy module Shutdown was called\n");
    }
    return( S_OK );
}
```

## -see-also

<a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy">ICertPolicy</a>



<a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy2">ICertPolicy2</a>
