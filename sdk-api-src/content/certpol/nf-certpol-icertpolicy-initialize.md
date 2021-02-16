---
UID: NF:certpol.ICertPolicy.Initialize
title: ICertPolicy::Initialize (certpol.h)
description: Called by the server engine to allow the policy module to perform initialization tasks.
helpviewer_keywords: ["CCertPolicy object [Security]","Initialize method","ICertPolicy interface [Security]","Initialize method","ICertPolicy.Initialize","ICertPolicy2 interface [Security]","Initialize method","ICertPolicy2::Initialize","ICertPolicy::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","CCertPolicy object","Initialize method [Security]","ICertPolicy interface","Initialize method [Security]","ICertPolicy2 interface","_certsrv_icertpolicy_initialize","certpol/ICertPolicy2::Initialize","certpol/ICertPolicy::Initialize","security.icertpolicy2_initialize","security.icertpolicy_initialize"]
old-location: security\icertpolicy2_initialize.htm
tech.root: security
ms.assetid: b0a0e9a6-79ca-4898-bddd-e736552aaf68
ms.date: 12/05/2018
ms.keywords: CCertPolicy object [Security],Initialize method, ICertPolicy interface [Security],Initialize method, ICertPolicy.Initialize, ICertPolicy2 interface [Security],Initialize method, ICertPolicy2::Initialize, ICertPolicy::Initialize, Initialize, Initialize method [Security], Initialize method [Security],CCertPolicy object, Initialize method [Security],ICertPolicy interface, Initialize method [Security],ICertPolicy2 interface, _certsrv_icertpolicy_initialize, certpol/ICertPolicy2::Initialize, certpol/ICertPolicy::Initialize, security.icertpolicy2_initialize, security.icertpolicy_initialize
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
 - ICertPolicy::Initialize
 - certpol/ICertPolicy::Initialize
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
 - ICertPolicy2.Initialize
 - ICertPolicy.Initialize
 - CCertPolicy.Initialize
---

# ICertPolicy::Initialize


## -description

The <b>Initialize</b> method is called by the server engine to allow the policy module to perform initialization tasks.

## -parameters

### -param strConfig [in]

Represents the name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig2">ICertConfig2</a>.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

When you write custom policy modules, implement this method.


#### Examples


```cpp
#include <windows.h>
#include <Certpol.h>

STDMETHODIMP CCertPolicy::Initialize(
    /* [in] */ BSTR const strConfig)
{
    // strConfig can be used by the Policy module.
    // Here, it is stored in a BSTR member variable.
    // m_strConfig is an application-defined variable.
    // Call SysFreeString to free m_strConfig when done.
    m_strConfig = SysAllocString( strConfig );
    // Check to determine whether there was enough memory.
    if (NULL == m_strConfig)
        return ( E_OUTOFMEMORY );  // Not enough memory

    return( S_OK );
}
```

## -see-also

<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>



<a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy">ICertPolicy</a>



<a href="/windows/desktop/api/certpol/nn-certpol-icertpolicy2">ICertPolicy2</a>