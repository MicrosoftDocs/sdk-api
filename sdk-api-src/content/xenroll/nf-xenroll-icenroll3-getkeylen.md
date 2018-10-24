---
UID: NF:xenroll.ICEnroll3.GetKeyLen
title: ICEnroll3::GetKeyLen
author: windows-sdk-content
description: Retrieves the minimum and maximum key lengths for the signature and exchange keys.
old-location: security\icenroll4_getkeylen.htm
tech.root: SecCrypto
ms.assetid: 9d4cde68-f47c-46ad-a0ca-ee287f6e5bed
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CEnroll object [Security],GetKeyLen method, GetKeyLen, GetKeyLen method [Security], GetKeyLen method [Security],CEnroll object, GetKeyLen method [Security],ICEnroll3 interface, GetKeyLen method [Security],ICEnroll4 interface, ICEnroll3 interface [Security],GetKeyLen method, ICEnroll3.GetKeyLen, ICEnroll3::GetKeyLen, ICEnroll4 interface [Security],GetKeyLen method, ICEnroll4::GetKeyLen, security.icenroll4_getkeylen, xenroll/ICEnroll3::GetKeyLen, xenroll/ICEnroll4::GetKeyLen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.GetKeyLen
 - ICEnroll3.GetKeyLen
 - CEnroll.GetKeyLen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll3::GetKeyLen


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetKeyLen</b> method retrieves the minimum and maximum key lengths for the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">signature</a> and <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange keys</a>. This method was first defined in the <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a> interface. The values retrieved by this method are dependent upon the current <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a>.


## -parameters




### -param fMin [in]

Boolean value indicating which key length (minimum or maximum) is retrieved. If <i>fMin</i> is <b>TRUE</b>, the minimum key length is retrieved; if it is <b>FALSE</b>, the maximum key length is retrieved.


### -param fExchange [in]

Boolean value indicating the type of key. If <i>fExchange</i> is <b>TRUE</b>, the exchange key length is retrieved; if it is <b>FALSE</b>, the signature key length is retrieved.


### -param pdwKeySize [out]

Pointer that receives the key's minimum or maximum length, in bits.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and *<i>pdwKeySize</i> will be the value representing the length (in bits) for the key's minimum or maximum length.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
A value that represents the length, in bits, for the key's minimum or maximum length.




## -remarks



Call this method to determine the minimum and maximum key lengths. If a CSP does not support this method, an error is returned.


#### Examples


```cpp
DWORD dwExchMin, dwExchMax, dwSignMin, dwSignMax;

// Determine the minimum and maximum key length values.
// hr is HRESULT variable.
hr = pEnroll->GetKeyLen( TRUE, TRUE, &dwExchMin );
if ( FAILED( hr ) )    
    printf("Failed GetKeyLen for Exchange Minimum [%x]\n", hr);
else
    printf("Exchange key Min: %d\n", dwExchMin);

hr = pEnroll->GetKeyLen( FALSE, TRUE, &dwExchMax );
if ( FAILED( hr ) )
    printf("Failed GetKeyLen for Exchange Maximum [%x]\n", hr);
else
    printf("Exchange key Max: %d\n", dwExchMax );

hr = pEnroll->GetKeyLen( TRUE, FALSE, &dwSignMin );
if ( FAILED( hr ) )
    printf("Failed GetKeyLen for Signature Minimum [%x]\n", hr);
else
    printf("Signature key Min: %d\n", dwSignMin );

hr = pEnroll->GetKeyLen( FALSE, FALSE, &dwSignMax );
if ( FAILED( hr ) )    
    printf("Failed GetKeyLen for Signature Maximum [%x]\n", hr);
else
    printf("Signature key Max: %d\n", dwSignMax );
```





## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

