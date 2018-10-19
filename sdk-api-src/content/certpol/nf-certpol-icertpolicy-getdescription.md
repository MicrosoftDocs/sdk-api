---
UID: NF:certpol.ICertPolicy.GetDescription
title: ICertPolicy::GetDescription
author: windows-sdk-content
description: Returns a human-readable description of the policy module and its function.
old-location: security\icertpolicy2_getdescription.htm
tech.root: seccrypto
ms.assetid: 38b85fa8-f5e7-4ac8-9f38-1cad83417797
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CCertPolicy object [Security],GetDescription method, GetDescription, GetDescription method [Security], GetDescription method [Security],CCertPolicy object, GetDescription method [Security],ICertPolicy interface, GetDescription method [Security],ICertPolicy2 interface, ICertPolicy interface [Security],GetDescription method, ICertPolicy.GetDescription, ICertPolicy2 interface [Security],GetDescription method, ICertPolicy2::GetDescription, ICertPolicy::GetDescription, _certsrv_icertpolicy_getdescription, certpol/ICertPolicy2::GetDescription, certpol/ICertPolicy::GetDescription, security.icertpolicy2_getdescription
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certidl.lib
 - Certidl.dll
api_name:
 - ICertPolicy2.GetDescription
 - ICertPolicy.GetDescription
 - CCertPolicy.GetDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPolicy::GetDescription


## -description


The <b>GetDescription</b> method returns a human-readable description of the policy module and its function.


## -parameters




### -param pstrDescription [out]

A pointer to a <b>BSTR</b> that describes the policy module.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a string that describes the policy module and its function.




## -remarks



When you write custom policy modules, implement this method.


#### Examples


```cpp
#include <windows.h>
#include <Certpol.h>

STDMETHODIMP CCertPolicy::GetDescription(
    /* [out, retval] */ BSTR __RPC_FAR *pstrDescription)
{
    if (NULL == pstrDescription)
    {
        // Bad pointer address
        return ( E_POINTER );
    }
    if (NULL != *pstrDescription)
    {
        SysFreeString(*pstrDescription);
        *pstrDescription=NULL;
    }
    // wszMyModuleDesc defined elsewhere, for example:
    // #define wszMyModuleDesc L"My Policy Module"
    *pstrDescription = SysAllocString(wszMyModuleDesc);
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




<a href="https://msdn.microsoft.com/en-us/library/Aa385033(v=VS.85).aspx">ICertPolicy</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385034(v=VS.85).aspx">ICertPolicy2</a>
 

 

