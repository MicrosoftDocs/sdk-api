---
UID: NF:certexit.ICertExit.GetDescription
title: ICertExit::GetDescription (certexit.h)
description: Returns a human-readable description of the exit module and its function.
helpviewer_keywords: ["CCertExit object [Security]","GetDescription method","GetDescription","GetDescription method [Security]","GetDescription method [Security]","CCertExit object","GetDescription method [Security]","ICertExit interface","GetDescription method [Security]","ICertExit2 interface","ICertExit interface [Security]","GetDescription method","ICertExit.GetDescription","ICertExit2 interface [Security]","GetDescription method","ICertExit2::GetDescription","ICertExit::GetDescription","_certsrv_icertexit_getdescription","certexit/ICertExit2::GetDescription","certexit/ICertExit::GetDescription","security.icertexit2_getdescription"]
old-location: security\icertexit2_getdescription.htm
tech.root: security
ms.assetid: 362d67c7-54ab-482e-9b2b-05ba1b6e2a70
ms.date: 12/05/2018
ms.keywords: CCertExit object [Security],GetDescription method, GetDescription, GetDescription method [Security], GetDescription method [Security],CCertExit object, GetDescription method [Security],ICertExit interface, GetDescription method [Security],ICertExit2 interface, ICertExit interface [Security],GetDescription method, ICertExit.GetDescription, ICertExit2 interface [Security],GetDescription method, ICertExit2::GetDescription, ICertExit::GetDescription, _certsrv_icertexit_getdescription, certexit/ICertExit2::GetDescription, certexit/ICertExit::GetDescription, security.icertexit2_getdescription
req.header: certexit.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertExit::GetDescription
 - certexit/ICertExit::GetDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certexit.h
api_name:
 - ICertExit2.GetDescription
 - ICertExit.GetDescription
 - CCertExit.GetDescription
---

# ICertExit::GetDescription


## -description

The <b>GetDescription</b> method returns a human-readable description of the exit module and its function. This method was first defined in the  <a href="/windows/desktop/api/certexit/nn-certexit-icertexit">ICertExit</a> interface.

## -parameters

### -param pstrDescription [out]

A pointer to the <b>BSTR</b> that describes the exit module.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a string that describes the exit module and its function.

## -remarks

When you write a custom exit module, implement this method.


#### Examples


```cpp
STDMETHODIMP
CCertExit::GetDescription(
    /* [out, retval] */ BSTR __RPC_FAR *pstrDescription)
{
    if (NULL == pstrDescription)
    {
        // Bad pointer address.
        return (E_POINTER);
    }
    if (NULL != *pstrDescription)
    {
        SysFreeString(*pstrDescription);
        *pstrDescription=NULL;
    }
    // wszMyExitModuleDesc defined elsewhere, for example:
    // #define wszMyExitModuleDesc L"My Exit Module"
    *pstrDescription = SysAllocString(wszMyExitModuleDesc);
    if (NULL == *pstrDescription)
    {
        // Not enough memory
        return ( E_OUTOFMEMORY );
    }
    // Success
    return( S_OK );
}
```

## -see-also

<a href="/windows/desktop/api/certexit/nn-certexit-icertexit">ICertExit</a>



<a href="/windows/desktop/api/certexit/nn-certexit-icertexit2">ICertExit2</a>