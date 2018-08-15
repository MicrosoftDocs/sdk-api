---
UID: NF:winscard.SCardGetCardTypeProviderNameA
title: SCardGetCardTypeProviderNameA function
author: windows-sdk-content
description: Returns the name of the module (dynamic link library) that contains the provider for a given card name and provider type.
old-location: security\scardgetcardtypeprovidername.htm
old-project: secauthn
ms.assetid: 5006d1d6-b0f4-431f-8868-d1f4fc0c8124
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SCARD_PROVIDER_CARD_MODULE, SCARD_PROVIDER_CSP, SCARD_PROVIDER_KSP, SCARD_PROVIDER_PRIMARY, SCardGetCardTypeProviderName, SCardGetCardTypeProviderName function [Security], SCardGetCardTypeProviderNameA, SCardGetCardTypeProviderNameW, _smart_scardgetcardtypeprovidername, security.scardgetcardtypeprovidername, winscard/SCardGetCardTypeProviderName, winscard/SCardGetCardTypeProviderNameA, winscard/SCardGetCardTypeProviderNameW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winscard.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WINSAT_BITMAP_SIZE
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
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardGetCardTypeProviderNameA function


## -description


The <b>SCardGetCardTypeProviderName</b> function returns the name of the module (dynamic link library) that contains the provider for a given card name and <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">provider type</a>.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context can be set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>. This value can be <b>NULL</b> if the call to <b>SCardGetCardTypeProviderName</b> is not directed to a specific <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a>.


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
The function retrieves the name of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card's</a> <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary service provider</a> as a GUID string.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROVIDER_CSP"></a><a id="scard_provider_csp"></a><dl>
<dt><b>SCARD_PROVIDER_CSP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The function retrieves the name of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROVIDER_KSP"></a><a id="scard_provider_ksp"></a><dl>
<dt><b>SCARD_PROVIDER_KSP</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The function retrieves the name of the smart card <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key storage provider</a> (KSP).

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

String variable to receive the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">provider name</a> upon successful completion of this function.


### -param pcchProvider [in, out]

Pointer to <b>DWORD</b> value. On input, <i>pcchProvider</i> supplies the length of the <i>szProvider</i> buffer in characters. If this value is SCARD_AUTOALLOCATE, then <i>szProvider</i> is converted to a pointer to a byte pointer and receives the address of a block of memory containing the string. This block of memory must be deallocated by calling 
<a href="https://msdn.microsoft.com/d41d3891-671b-4129-8034-b251af983830">SCardFreeMemory</a>. 




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
<a href="authentication_return_values.htm">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



This function is not redirected, but calling the function when inside a Remote Desktop session  will not result in an error. It only means that the result will be from the remote computer instead of the local computer. 

Upon successful completion of this function, the value in <i>szProvider</i> can be used as the third parameter in a call to 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>.


#### Examples

The following example shows how to retrieve the provider name for the specified reader context. The example assumes that hContext is a valid handle obtained from a previous call to the <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LPTSTR szProvider = NULL;
LPTSTR szCardName = _T("WindowsCard");
DWORD  chProvider = SCARD_AUTOALLOCATE;
LONG   lReturn = SCARD_S_SUCCESS;

// Retrieve the provider name.
// hContext was set by SCardEstablishContext.
lReturn = SCardGetCardTypeProviderName(hContext,
                                       szCardName,
                                       SCARD_PROVIDER_CSP,
                                       (LPTSTR)&amp;szProvider,
                                       &amp;chProvider);
if (SCARD_S_SUCCESS == lReturn)
{
    BOOL fSts = TRUE;
    HCRYPTPROV hProv = NULL;
  
  // Acquire a Cryptographic operation context.
    fSts = CryptAcquireContext(&amp;hProv,
                               NULL,
                               szProvider,
                               PROV_RSA_FULL,
                               0);
    // Perform Cryptographic operations with smart card
    // ...

    // Free memory allocated by SCardGetCardTypeProviderName.
    lReturn = SCardFreeMemory(hContext, szProvider);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/d41d3891-671b-4129-8034-b251af983830">SCardFreeMemory</a>



<a href="https://msdn.microsoft.com/c36dfb77-6ebe-4073-b657-72fa294b5464">SCardSetCardTypeProviderName</a>
 

 

