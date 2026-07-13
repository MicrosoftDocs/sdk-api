---
UID: NF:winscard.SCardListCardsA
title: SCardListCardsA function (winscard.h)
description: Searches the smart card database and provides a list of named cards previously introduced to the system by the user. (ANSI)
helpviewer_keywords: ["SCardListCardsA", "winscard/SCardListCardsA"]
old-location: security\scardlistcards.htm
tech.root: security
ms.assetid: b8ecbb8c-e1fb-485b-9a2c-20e6edf25cf1
ms.date: 12/05/2018
ms.keywords: SCardListCards, SCardListCards function [Security], SCardListCardsA, SCardListCardsW, _smart_scardlistcards, security.scardlistcards, winscard/SCardListCards, winscard/SCardListCardsA, winscard/SCardListCardsW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardListCardsW (Unicode) and SCardListCardsA (ANSI)
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
 - SCardListCardsA
 - winscard/SCardListCardsA
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
 - SCardListCards
 - SCardListCardsA
 - SCardListCardsW
---

# SCardListCardsA function


## -description

The <b>SCardListCards</b> function searches the <a href="/windows/desktop/SecGloss/s-gly">smart card database</a> and provides a list of named cards previously introduced to the system by the user.

The caller specifies an <a href="/windows/desktop/SecGloss/a-gly">ATR string</a>, a set of interface identifiers (GUIDs), or both. If both an ATR string and an identifier array are supplied, the cards returned will match the ATR string supplied and support the interfaces specified.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a> for the query. The resource manager context can be set by a previous call to <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>.

If this parameter is set to <b>NULL</b>, the search for cards is not limited to any context.

### -param pbAtr [in, optional]

Address of an ATR string to compare to known cards, or <b>NULL</b> if no ATR matching is to be performed.

### -param rgquidInterfaces [in]

Array of identifiers (GUIDs), or <b>NULL</b> if no interface matching is to be performed. When an array is supplied, a card name will be returned only if all the specified identifiers are supported by the card.

### -param cguidInterfaceCount [in]

Number of entries in the <i>rgguidInterfaces</i> array. If <i>rgguidInterfaces</i> is <b>NULL</b>, then this value is ignored.

### -param mszCards [out]

Multi-string that lists the <a href="/windows/desktop/SecGloss/s-gly">smart cards</a> found. If this value is <b>NULL</b>, <b>SCardListCards</b> ignores the buffer length supplied in <i>pcchCards</i>, returning the length of the buffer that would have been returned if this parameter had not been <b>NULL</b> to <i>pcchCards</i> and a success code.

### -param pcchCards [in, out]

Length of the <i>mszCards</i> buffer in characters. Receives the actual length of the multi-string structure, including all trailing <b>null</b> characters. If the buffer length is specified as SCARD_AUTOALLOCATE, then <i>mszCards</i> is converted to a pointer to a byte pointer, and receives the address of a block of memory containing the multi-string structure. This block of memory must be deallocated with 
<a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a>.

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

To return all smart cards introduced to the subsystem, set <i>pbAtr</i> and <i>rgguidInterfaces</i> to <b>NULL</b>.

The <b>SCardListCards</b> function is a database query function. For more information on other database query functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-query-functions">Smart Card Database Query Functions</a>.

Calling this function should be done outside of a transaction. If an application begins a transaction with the <a href="/windows/desktop/api/winscard/nf-winscard-scardbegintransaction">SCardBeginTransaction</a> function and then calls this function, it resets the <i>hCard</i> parameter (of type <b>SCARDHANDLE</b>) of the <b>SCardBeginTransaction</b> function.

<b>Windows Server 2008 R2 and Windows 7:  </b>Calling this function within a transaction could result in your computer becoming unresponsive.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>Not applicable.


#### Examples

The following example  shows listing of the smart cards.


```cpp
LPTSTR pmszCards = NULL;
LPTSTR pCard;
LONG lReturn;
DWORD cch = SCARD_AUTOALLOCATE;

// Retrieve the list of cards.
lReturn = SCardListCards(NULL,
                         NULL,
                         NULL,
                         NULL,
                         (LPTSTR)&pmszCards,
                         &cch );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardListCards\n");
    exit(1); // Or other appropriate error action
}
// Do something with the multi string of cards.
// Output the values.
// A double-null terminates the list of values.
pCard = pmszCards;
while ( '\0' != *pCard )
{
    // Display the value.
    printf("%S\n", pCard );
    // Advance to the next value.
    pCard = pCard + wcslen(pCard) + 1;
}

// Remember to free pmszCards (by calling SCardFreeMemory).
// ...

```






> [!NOTE]
> The winscard.h header defines SCardListCards as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardgetproviderida">SCardGetProviderId</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistinterfacesa">SCardListInterfaces</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistreadergroupsa">SCardListReaderGroups</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistreadersa">SCardListReaders</a>
