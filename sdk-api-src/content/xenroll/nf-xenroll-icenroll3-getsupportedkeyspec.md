---
UID: NF:xenroll.ICEnroll3.GetSupportedKeySpec
title: ICEnroll3::GetSupportedKeySpec (xenroll.h)
description: Retrieves information regarding the current cryptographic service provider (CSP) support for signature and/or exchange operations. This method was first defined in the ICEnroll3 interface.
helpviewer_keywords: ["CEnroll object [Security]","GetSupportedKeySpec method","GetSupportedKeySpec","GetSupportedKeySpec method [Security]","GetSupportedKeySpec method [Security]","CEnroll object","GetSupportedKeySpec method [Security]","ICEnroll3 interface","GetSupportedKeySpec method [Security]","ICEnroll4 interface","ICEnroll3 interface [Security]","GetSupportedKeySpec method","ICEnroll3.GetSupportedKeySpec","ICEnroll3::GetSupportedKeySpec","ICEnroll4 interface [Security]","GetSupportedKeySpec method","ICEnroll4::GetSupportedKeySpec","security.icenroll4_getsupportedkeyspec","xenroll/ICEnroll3::GetSupportedKeySpec","xenroll/ICEnroll4::GetSupportedKeySpec"]
old-location: security\icenroll4_getsupportedkeyspec.htm
tech.root: security
ms.assetid: e225eddb-0c36-446a-9696-38653ff22511
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],GetSupportedKeySpec method, GetSupportedKeySpec, GetSupportedKeySpec method [Security], GetSupportedKeySpec method [Security],CEnroll object, GetSupportedKeySpec method [Security],ICEnroll3 interface, GetSupportedKeySpec method [Security],ICEnroll4 interface, ICEnroll3 interface [Security],GetSupportedKeySpec method, ICEnroll3.GetSupportedKeySpec, ICEnroll3::GetSupportedKeySpec, ICEnroll4 interface [Security],GetSupportedKeySpec method, ICEnroll4::GetSupportedKeySpec, security.icenroll4_getsupportedkeyspec, xenroll/ICEnroll3::GetSupportedKeySpec, xenroll/ICEnroll4::GetSupportedKeySpec
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICEnroll3::GetSupportedKeySpec
 - xenroll/ICEnroll3::GetSupportedKeySpec
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.GetSupportedKeySpec
 - ICEnroll3.GetSupportedKeySpec
 - CEnroll.GetSupportedKeySpec
---

# ICEnroll3::GetSupportedKeySpec


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetSupportedKeySpec</b> method retrieves information regarding the current <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) support for signature and/or exchange operations. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a> interface.

The values retrieved by this method are dependent upon the current CSP.

## -parameters

### -param pdwKeySpec [out]

A pointer to a <b>LONG</b> that receives a bit flag that indicates whether the current CSP supports <a href="/windows/desktop/SecGloss/e-gly">exchange</a> and <a href="/windows/desktop/SecGloss/s-gly">signature keys</a>.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a value that indicates whether the current CSP supports exchange and signature keys. If the CSP does not support this method, an error is returned.

## -remarks

Call this method to determine whether the current CSP supports exchange keys, signature keys, or both. The <i>pdwKeySpec</i> parameter will contain one or more of the following constants (defined in Wincrypt.h):<ul>
<li>AT_KEYEXCHANGE</li>
<li>AT_SIGNATURE</li>
</ul>



#### Examples


```cpp
DWORD dwKeySpec;

// Determine the supported key specifications.
// hr is HRESULT variable.
hr = pEnroll->GetSupportedKeySpec( &dwKeySpec );
if ( FAILED( hr ) )    
    printf("Failed GetSupportedKeySpec [%x]\n", hr);
else
{
    printf("Exchange keys are %s. Signature keys are %s.\n",
           dwKeySpec & AT_KEYEXCHANGE ? "supported" : "not supported",
           dwKeySpec & AT_SIGNATURE ? "supported" : "not supported" );
}
```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>