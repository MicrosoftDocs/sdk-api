---
UID: NF:winscard.SCardLocateCardsW
title: SCardLocateCardsW function (winscard.h)
description: Searches the readers listed in the rgReaderStates parameter for a card with an ATR string that matches one of the card names specified in mszCards, returning immediately with the result. (Unicode)
helpviewer_keywords: ["SCardLocateCards", "SCardLocateCards function [Security]", "SCardLocateCardsW", "_smart_scardlocatecards", "security.scardlocatecards", "winscard/SCardLocateCards", "winscard/SCardLocateCardsW"]
old-location: security\scardlocatecards.htm
tech.root: security
ms.assetid: 7ee90188-6fe5-417b-a7c7-9c29d9cdd4d0
ms.date: 12/05/2018
ms.keywords: SCardLocateCards, SCardLocateCards function [Security], SCardLocateCardsA, SCardLocateCardsW, _smart_scardlocatecards, security.scardlocatecards, winscard/SCardLocateCards, winscard/SCardLocateCardsA, winscard/SCardLocateCardsW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardLocateCardsW (Unicode) and SCardLocateCardsA (ANSI)
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
 - SCardLocateCardsW
 - winscard/SCardLocateCardsW
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
 - SCardLocateCards
 - SCardLocateCardsA
 - SCardLocateCardsW
---

# SCardLocateCardsW function


## -description

The <b>SCardLocateCards</b> function searches the readers listed in the <i>rgReaderStates</i> parameter for a card with an <a href="/windows/desktop/SecGloss/a-gly">ATR string</a> that matches one of the card names specified in <i>mszCards</i>, returning immediately with the result.

## -parameters

### -param hContext [in]

A handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>.

### -param mszCards [in]

A multiple string that contains the names of the cards to search for.

### -param rgReaderStates [in, out]

An array of <a href="/windows/desktop/api/winscard/ns-winscard-scard_readerstatea">SCARD_READERSTATE</a> structures that, on input, specify the readers to search and that, on output, receives the result.

### -param cReaders [in]

The number of elements in the <i>rgReaderStates</i> array.

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

This service is especially useful when used in conjunction with 
<a href="/windows/desktop/api/winscard/nf-winscard-scardgetstatuschangea">SCardGetStatusChange</a>. If no matching cards are found by means of <b>SCardLocateCards</b>, the calling application may use <b>SCardGetStatusChange</b> to wait for card availability changes.

The <b>SCardLocateCards</b> function is a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> tracking function. For more information on other tracking functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-tracking-functions">Smart Card Tracking Functions</a>.

Calling this function should be done outside of a transaction. If an application begins a transaction with the <a href="/windows/desktop/api/winscard/nf-winscard-scardbegintransaction">SCardBeginTransaction</a> function and then calls this function, it resets the <i>hCard</i> parameter (of type <b>SCARDHANDLE</b>) of the <b>SCardBeginTransaction</b> function.

<b>Windows Server 2008 R2 and Windows 7:  </b>Calling this function within a transaction could result in your computer becoming unresponsive.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>Not applicable.


#### Examples

The following example  shows locating smart cards.


```cpp
// Copyright (C) Microsoft. All rights reserved. 
#include <stdio.h>
#include <winscard.h>
#include <tchar.h>
#pragma comment(lib, "winscard.lib")

HRESULT __cdecl main()
{
HRESULT           hr = S_OK;
LPTSTR            szReaders, szRdr;
DWORD             cchReaders = SCARD_AUTOALLOCATE;
DWORD             dwI, dwRdrCount;
SCARD_READERSTATE rgscState[MAXIMUM_SMARTCARD_READERS];
TCHAR             szCard[MAX_PATH];
SCARDCONTEXT      hSC;
LONG              lReturn;

// Establish the card to watch for.
// Multiple cards can be looked for, but
// this sample looks for only one card.
_tcscat_s ( szCard, MAX_PATH * sizeof(TCHAR), TEXT("GemSAFE"));
szCard[lstrlen(szCard) + 1] = 0;  // Double trailing zero.

// Establish a context.
lReturn = SCardEstablishContext(SCARD_SCOPE_USER,
                                NULL,
                                NULL,
                                &hSC );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardEstablishContext\n");
    exit(1);
}

// Determine which readers are available.
lReturn = SCardListReaders(hSC,
                           NULL,
                           (LPTSTR)&szReaders,
                           &cchReaders );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardListReaders\n");
    exit(1);
}
// Place the readers into the state array.
szRdr = szReaders;
for ( dwI = 0; dwI < MAXIMUM_SMARTCARD_READERS; dwI++ )
{
    if ( 0 == *szRdr )
        break;
    rgscState[dwI].szReader = szRdr;
    rgscState[dwI].dwCurrentState = SCARD_STATE_UNAWARE;
    szRdr += lstrlen(szRdr) + 1;
}
dwRdrCount = dwI;

// If any readers are available, proceed.
if ( 0 != dwRdrCount )
{
  for (;;)
  { 
    // Look for the card.
    lReturn = SCardLocateCards(hSC,
                               szCard,
                               rgscState,
                               dwRdrCount );
    if ( SCARD_S_SUCCESS != lReturn )
    {
        printf("Failed SCardLocateCards\n");
        exit(1);
    }

    // Look through the array of readers.
    for ( dwI=0; dwI < dwRdrCount; dwI++)
    {
        if ( 0 != ( SCARD_STATE_ATRMATCH & 
                    rgscState[dwI].dwEventState))
        {
           _tprintf( TEXT("Card '%s' found in reader '%s'.\n"),
                     szCard,
                     rgscState[dwI].szReader );
            SCardFreeMemory( hSC,
                             szReaders );
            return 0;  // Context will be release automatically.
        }
        // Update the state.
        rgscState[dwI].dwCurrentState = rgscState[dwI].dwEventState;
    }

  // Card not found yet; wait until there is a change.
  lReturn = SCardGetStatusChange(hSC,
                                 INFINITE, // infinite wait
                                 rgscState,
                                 dwRdrCount );
  if ( SCARD_S_SUCCESS != lReturn )
  {
    printf("Failed SCardGetStatusChange\n");
    exit(1);
  }
 }  // for (;;)
}
else
    printf("No readers available\n");

// Release the context.
lReturn = SCardReleaseContext(hSC);
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardReleaseContext\n");
    exit(1);
}

SCardFreeMemory( hSC,
                 szReaders );

return hr;
}

```






> [!NOTE]
> The winscard.h header defines SCardLocateCards as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/ns-winscard-scard_readerstatea">SCARD_READERSTATE</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardcancel">SCardCancel</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardgetstatuschangea">SCardGetStatusChange</a>
