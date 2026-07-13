---
UID: NF:winscard.SCardGetCardTypeProviderNameA
title: SCardGetCardTypeProviderNameA function (winscard.h)
description: Returns the name of the module (dynamic link library) that contains the provider for a given card name and provider type. (ANSI)
helpviewer_keywords: ["SCARD_PROVIDER_CARD_MODULE", "SCARD_PROVIDER_CSP", "SCARD_PROVIDER_KSP", "SCARD_PROVIDER_PRIMARY", "SCardGetCardTypeProviderNameA", "winscard/SCardGetCardTypeProviderNameA"]
old-location: security\scardgetcardtypeprovidername.htm
tech.root: security
ms.assetid: 5006d1d6-b0f4-431f-8868-d1f4fc0c8124
ms.date: 12/05/2018
ms.keywords: SCARD_PROVIDER_CARD_MODULE, SCARD_PROVIDER_CSP, SCARD_PROVIDER_KSP, SCARD_PROVIDER_PRIMARY, SCardGetCardTypeProviderName, SCardGetCardTypeProviderName function [Security], SCardGetCardTypeProviderNameA, SCardGetCardTypeProviderNameW, _smart_scardgetcardtypeprovidername, security.scardgetcardtypeprovidername, winscard/SCardGetCardTypeProviderName, winscard/SCardGetCardTypeProviderNameA, winscard/SCardGetCardTypeProviderNameW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardGetCardTypeProviderNameW (Unicode) and SCardGetCardTypeProviderNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardGetCardTypeProviderNameA
 - winscard/SCardGetCardTypeProviderNameA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
 - Ext-MS-Win-wlan-scard-l1-1-0.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardGetCardTypeProviderName
 - SCardGetCardTypeProviderNameA
 - SCardGetCardTypeProviderNameW
---

# SCardGetCardTypeProviderNameA function


## -description

The <b>SCardGetCardTypeProviderName</b> function returns the name of the module (dynamic link library) that contains the provider for a given card name and <a href="/windows/desktop/SecGloss/p-gly">provider type</a>.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context can be set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. This value can be <b>NULL</b> if the call to <b>SCardGetCardTypeProviderName</b> is not directed to a specific <a href="/windows/desktop/SecGloss/c-gly">context</a>.

### -param szCardName [in]

Name of the card type with which this provider name is associated.

### -param dwProviderId [in]

Identifier for the provider associated with this card type. 
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROVIDER_PRIMARY"></a><a id="scard_provider_primary"></a><dl>
<dt><b>SCARD_PROVIDER_PRIMARY</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The function retrieves the name of the <a href="/windows/desktop/SecGloss/s-gly">smart card's</a> <a href="/windows/desktop/SecGloss/p-gly">primary service provider</a> as a GUID string.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROVIDER_CSP"></a><a id="scard_provider_csp"></a><dl>
<dt><b>SCARD_PROVIDER_CSP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The function retrieves the name of the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROVIDER_KSP"></a><a id="scard_provider_ksp"></a><dl>
<dt><b>SCARD_PROVIDER_KSP</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The function retrieves the name of the smart card <a href="/windows/desktop/SecGloss/k-gly">key storage provider</a> (KSP).

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROVIDER_CARD_MODULE"></a><a id="scard_provider_card_module"></a><dl>
<dt><b>SCARD_PROVIDER_CARD_MODULE</b></dt>
<dt>0x80000001</dt>
</dl>
</td>
<td width="60%">
The function retrieves the name of the card module.

</td>
</tr>
</table>

### -param szProvider [out]

String variable to receive the <a href="/windows/desktop/SecGloss/p-gly">provider name</a> upon successful completion of this function.

### -param pcchProvider [in, out]

Pointer to <b>DWORD</b> value. On input, <i>pcchProvider</i> supplies the length of the <i>szProvider</i> buffer in characters. If this value is SCARD_AUTOALLOCATE, then <i>szProvider</i> is converted to a pointer to a byte pointer and receives the address of a block of memory containing the string. This block of memory must be deallocated by calling 
<a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a>. 




On output, this value represents the actual number of characters, including the <b>null</b> terminator, in the <i>szProvider</i> variable.

## -returns

This function returns different values depending on whether it succeeds or fails.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Success</b></dt>
</dl>
</td>
<td width="60%">
SCARD_S_SUCCESS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Failure</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

</td>
</tr>
</table>

## -remarks

This function is not redirected, but calling the function when inside a Remote Desktop session  will not result in an error. It only means that the result will be from the remote computer instead of the local computer. 

Upon successful completion of this function, the value in <i>szProvider</i> can be used as the third parameter in a call to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>.


#### Examples

The following example shows how to retrieve the provider name for the specified reader context. The example assumes that hContext is a valid handle obtained from a previous call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> function.


```cpp
LPTSTR szProvider = NULL;
LPTSTR szCardName = _T("WindowsCard");
DWORD  chProvider = SCARD_AUTOALLOCATE;
LONG   lReturn = SCARD_S_SUCCESS;

// Retrieve the provider name.
// hContext was set by SCardEstablishContext.
lReturn = SCardGetCardTypeProviderName(hContext,
                                       szCardName,
                                       SCARD_PROVIDER_CSP,
                                       (LPTSTR)&szProvider,
                                       &chProvider);
if (SCARD_S_SUCCESS == lReturn)
{
    BOOL fSts = TRUE;
    HCRYPTPROV hProv = NULL;
  
  // Acquire a Cryptographic operation context.
    fSts = CryptAcquireContext(&hProv,
                               NULL,
                               szProvider,
                               PROV_RSA_FULL,
                               0);
    // Perform Cryptographic operations with smart card
    // ...

    // Free memory allocated by SCardGetCardTypeProviderName.
    lReturn = SCardFreeMemory(hContext, szProvider);
}

```






> [!NOTE]
> The winscard.h header defines SCardGetCardTypeProviderName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardsetcardtypeprovidernamea">SCardSetCardTypeProviderName</a>
