---
UID: NF:winscard.SCardSetCardTypeProviderNameW
title: SCardSetCardTypeProviderNameW function (winscard.h)
description: Specifies the name of the module (dynamic link library) containing the provider for a given card name and provider type. (Unicode)
helpviewer_keywords: ["SCARD_PROVIDER_CARD_MODULE", "SCARD_PROVIDER_CSP", "SCARD_PROVIDER_KSP", "SCARD_PROVIDER_PRIMARY", "SCardSetCardTypeProviderName", "SCardSetCardTypeProviderName function [Security]", "SCardSetCardTypeProviderNameW", "_smart_scardsetcardtypeprovidername", "security.scardsetcardtypeprovidername", "winscard/SCardSetCardTypeProviderName", "winscard/SCardSetCardTypeProviderNameW"]
old-location: security\scardsetcardtypeprovidername.htm
tech.root: security
ms.assetid: c36dfb77-6ebe-4073-b657-72fa294b5464
ms.date: 12/05/2018
ms.keywords: SCARD_PROVIDER_CARD_MODULE, SCARD_PROVIDER_CSP, SCARD_PROVIDER_KSP, SCARD_PROVIDER_PRIMARY, SCardSetCardTypeProviderName, SCardSetCardTypeProviderName function [Security], SCardSetCardTypeProviderNameA, SCardSetCardTypeProviderNameW, _smart_scardsetcardtypeprovidername, security.scardsetcardtypeprovidername, winscard/SCardSetCardTypeProviderName, winscard/SCardSetCardTypeProviderNameA, winscard/SCardSetCardTypeProviderNameW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardSetCardTypeProviderNameW (Unicode) and SCardSetCardTypeProviderNameA (ANSI)
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
 - SCardSetCardTypeProviderNameW
 - winscard/SCardSetCardTypeProviderNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
api_name:
 - SCardSetCardTypeProviderName
 - SCardSetCardTypeProviderNameA
 - SCardSetCardTypeProviderNameW
---

# SCardSetCardTypeProviderNameW function


## -description

The <b>SCardSetCardTypeProviderName</b> function specifies the name of the module (dynamic link library) containing the provider for a given card name and <a href="/windows/desktop/SecGloss/p-gly">provider type</a>.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context can be set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. This value can be <b>NULL</b> if the call to <b>SCardSetCardTypeProviderName</b> is not directed to a specific <a href="/windows/desktop/SecGloss/c-gly">context</a>.

### -param szCardName [in]

Name of the card type with which this <a href="/windows/desktop/SecGloss/p-gly">provider name</a> is associated.

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
The function retrieves the name of the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).

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

### -param szProvider [in]

A string that contains the provider name that is representing the CSP.

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

This function is not redirected, but calling the function  when inside a Remote Desktop session  will not result in an error. It only means that the result will be from the remote computer instead of the local computer. 

This function sets the provider name, while 
<a href="/windows/desktop/api/winscard/nf-winscard-scardgetcardtypeprovidernamea">SCardGetCardTypeProviderName</a> can be used to retrieve the provider name.


#### Examples

The following example  shows how to specify the card type provider name.


```cpp
LPTSTR            szNewProvName = _T("My Provider Name");
LPTSTR            szCardName = _T("WindowsCard");
LONG              lReturn = SCARD_S_SUCCESS;

// Set the card type provider name.
// hContext was set by SCardEstablishContext.
lReturn = SCardSetCardTypeProviderName(hContext,
                                      szCardName,
                                      SCARD_PROVIDER_CSP,
                                      szNewProvName);
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardSetCardTypeProviderName - %x\n", lReturn);
    exit(1);
}

```






> [!NOTE]
> The winscard.h header defines SCardSetCardTypeProviderName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardgetcardtypeprovidernamea">SCardGetCardTypeProviderName</a>
