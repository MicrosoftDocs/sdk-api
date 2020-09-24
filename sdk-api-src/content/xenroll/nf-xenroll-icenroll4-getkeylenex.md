---
UID: NF:xenroll.ICEnroll4.GetKeyLenEx
title: ICEnroll4::GetKeyLenEx (xenroll.h)
description: Retrieves size information for the signature and exchange keys. This method was first defined in the ICEnroll4 interface.
helpviewer_keywords: ["CEnroll object [Security]","GetKeyLenEx method","GetKeyLenEx","GetKeyLenEx method [Security]","GetKeyLenEx method [Security]","CEnroll object","GetKeyLenEx method [Security]","ICEnroll4 interface","ICEnroll4 interface [Security]","GetKeyLenEx method","ICEnroll4.GetKeyLenEx","ICEnroll4::GetKeyLenEx","XEKL_KEYSIZE_INC","XEKL_KEYSIZE_MAX","XEKL_KEYSIZE_MIN","XEKL_KEYSPEC_KEYX","XEKL_KEYSPEC_SIG","_xen_icenroll4_getkeylenex","security.icenroll4_getkeylenex","xenroll/ICEnroll4::GetKeyLenEx"]
old-location: security\icenroll4_getkeylenex.htm
tech.root: security
ms.assetid: 4e54926f-f600-4795-b6d8-efb146edcda2
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],GetKeyLenEx method, GetKeyLenEx, GetKeyLenEx method [Security], GetKeyLenEx method [Security],CEnroll object, GetKeyLenEx method [Security],ICEnroll4 interface, ICEnroll4 interface [Security],GetKeyLenEx method, ICEnroll4.GetKeyLenEx, ICEnroll4::GetKeyLenEx, XEKL_KEYSIZE_INC, XEKL_KEYSIZE_MAX, XEKL_KEYSIZE_MIN, XEKL_KEYSPEC_KEYX, XEKL_KEYSPEC_SIG, _xen_icenroll4_getkeylenex, security.icenroll4_getkeylenex, xenroll/ICEnroll4::GetKeyLenEx
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
 - ICEnroll4::GetKeyLenEx
 - xenroll/ICEnroll4::GetKeyLenEx
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
 - ICEnroll4.GetKeyLenEx
 - CEnroll.GetKeyLenEx
---

# ICEnroll4::GetKeyLenEx


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetKeyLenEx</b> method retrieves size information for the <a href="/windows/desktop/SecGloss/s-gly">signature</a> and <a href="/windows/desktop/SecGloss/e-gly">exchange keys</a>. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

The values retrieved by this method are dependent upon the current <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).

## -parameters

### -param lSizeSpec [in]

A value that indicates the type of size information to be retrieved. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSIZE_MIN"></a><a id="xekl_keysize_min"></a><dl>
<dt><b>XEKL_KEYSIZE_MIN</b></dt>
</dl>
</td>
<td width="60%">
The minimum key size.

</td>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSIZE_MAX"></a><a id="xekl_keysize_max"></a><dl>
<dt><b>XEKL_KEYSIZE_MAX</b></dt>
</dl>
</td>
<td width="60%">
The maximum key size.

</td>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSIZE_INC"></a><a id="xekl_keysize_inc"></a><dl>
<dt><b>XEKL_KEYSIZE_INC</b></dt>
</dl>
</td>
<td width="60%">
The size of the key increment. For more information, see Remarks.

</td>
</tr>
</table>

### -param lKeySpec [in]

Specifies the key for which size information is returned. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSPEC_KEYX"></a><a id="xekl_keyspec_keyx"></a><dl>
<dt><b>XEKL_KEYSPEC_KEYX</b></dt>
</dl>
</td>
<td width="60%">
Exchange key

</td>
</tr>
<tr>
<td width="40%"><a id="XEKL_KEYSPEC_SIG"></a><a id="xekl_keyspec_sig"></a><dl>
<dt><b>XEKL_KEYSPEC_SIG</b></dt>
</dl>
</td>
<td width="60%">
Signature key

</td>
</tr>
</table>

### -param pdwKeySize [out]

A pointer to a variable that receives the key size, in bits.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 A value that represents the key size, in bits.

## -remarks

If the CSP does not support this method, an error is returned.

For more information about the XEKL_KEYSIZE_INC value, see PP_SIG_KEYSIZE_INC usage in the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a> reference page.


#### Examples


```cpp
DWORD dwExchMin, dwExchMax, dwSignDef, dwSignInc;

// Determine the minimum and maximum key length values.
// hr is HRESULT variable.
hr = pEnroll4->GetKeyLenEx( XEKL_KEYSIZE_MIN,
                            XEKL_KEYSPEC_KEYX,
                            &dwExchMin );
if ( FAILED( hr ) )    
    printf("Failed GetKeyLenEx for Exchange Minimum [%x]\n", hr);
else
    printf("Exchange key Min: %d\n", dwExchMin);

hr = pEnroll4->GetKeyLenEx( XEKL_KEYSIZE_MAX,
                            XEKL_KEYSPEC_KEYX,
                            &dwExchMax );
if ( FAILED( hr ) )
    printf("Failed GetKeyLenEx for Exchange Maximum [%x]\n", hr);
else
    printf("Exchange key Max: %d\n", dwExchMax );

hr = pEnroll4->GetKeyLenEx( XEKL_KEYSIZE_DEFAULT,
                            XEKL_KEYSPEC_SIG,
                            &dwSignDef );
if ( FAILED( hr ) )
    printf("Failed GetKeyLenEx for Signature Default "
   "Key size [%x]\n", hr);
else
    printf("Signature key default size: %d\n", dwSignDef );

hr = pEnroll4->GetKeyLenEx( XEKL_KEYSIZE_INC,
                            XEKL_KEYSPEC_SIG,
                            &dwSignInc );
if ( FAILED( hr ) )    
    printf("Failed GetKeyLenEx for Signature "
   "Key Size Increment [%x]\n", hr);
else
    printf("Signature key increment size: %d\n", dwSignInc );
```