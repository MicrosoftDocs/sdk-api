---
UID: NF:winscard.SCardGetProviderIdW
title: SCardGetProviderIdW function (winscard.h)
description: Returns the identifier (GUID) of the primary service provider for a given card. (Unicode)
helpviewer_keywords: ["SCardGetProviderId", "SCardGetProviderId function [Security]", "SCardGetProviderIdW", "_smart_scardgetproviderid", "security.scardgetproviderid", "winscard/SCardGetProviderId", "winscard/SCardGetProviderIdW"]
old-location: security\scardgetproviderid.htm
tech.root: security
ms.assetid: 6e0f42af-9ac1-469b-b241-939d64676d99
ms.date: 12/05/2018
ms.keywords: SCardGetProviderId, SCardGetProviderId function [Security], SCardGetProviderIdA, SCardGetProviderIdW, _smart_scardgetproviderid, security.scardgetproviderid, winscard/SCardGetProviderId, winscard/SCardGetProviderIdA, winscard/SCardGetProviderIdW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardGetProviderIdW (Unicode) and SCardGetProviderIdA (ANSI)
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
 - SCardGetProviderIdW
 - winscard/SCardGetProviderIdW
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
 - SCardGetProviderId
 - SCardGetProviderIdA
 - SCardGetProviderIdW
---

# SCardGetProviderIdW function


## -description

The <b>SCardGetProviderId</b> function returns the identifier (GUID) of the <a href="/windows/desktop/SecGloss/p-gly">primary service provider</a> for a given card.

The caller supplies the name of a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> (previously introduced to the system) and receives the registered identifier of the primary service provider GUID, if one exists.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a> for the query. The resource manager context can be set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.

### -param szCard [in]

Name of the card defined to the system.

### -param pguidProviderId [out]

Identifier (GUID) of the primary service provider. This provider may be activated using COM, and will supply access to other services in the card.

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

The <b>SCardGetProviderId</b> function is a database query function. For more information on other database query functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-query-functions">Smart Card Database Query Functions</a>.


#### Examples

The following example shows how to get the provider ID for the specified card. The example assumes that hContext is a valid handle obtained from a previous call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> function and that "MyCardName" was introduced by a previous call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardintroducecardtypea">SCardIntroduceCardType</a> function.


```cpp
GUID    guidProv;
LONG    lReturn;

lReturn = SCardGetProviderId(hContext, 
                             L"MyCardName",
                             &guidProv);
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardGetProviderId - %x\n", lReturn);
else
{
    // Use the provider GUID as needed.
    // ...
}

```






> [!NOTE]
> The winscard.h header defines SCardGetProviderId as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistcardsa">SCardListCards</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistinterfacesa">SCardListInterfaces</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistreadergroupsa">SCardListReaderGroups</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistreadersa">SCardListReaders</a>
