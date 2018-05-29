---
UID: NF:winscard.SCardLocateCardsW
title: SCardLocateCardsW function
author: windows-sdk-content
description: Searches the readers listed in the rgReaderStates parameter for a card with an ATR string that matches one of the card names specified in mszCards, returning immediately with the result.
old-location: security\scardlocatecards.htm
old-project: SecAuthN
ms.assetid: 7ee90188-6fe5-417b-a7c7-9c29d9cdd4d0
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SCardLocateCards, SCardLocateCards function [Security], SCardLocateCardsA, SCardLocateCardsW, _smart_scardlocatecards, security.scardlocatecards, winscard/SCardLocateCards, winscard/SCardLocateCardsA, winscard/SCardLocateCardsW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winscard.dll
api_name:
-	SCardLocateCards
-	SCardLocateCardsA
-	SCardLocateCardsW
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardLocateCardsW function


## -description



			The <b>SCardLocateCards</b> function searches the readers listed in the <i>rgReaderStates</i> parameter for a card with an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ATR string</a> that matches one of the card names specified in <i>mszCards</i>, returning immediately with the result.


## -parameters




### -param hContext [in]

A handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>.


### -param mszCards [in]

A multiple string that contains the names of the cards to search for.


### -param rgReaderStates [in, out]

An array of <a href="https://msdn.microsoft.com/4e9bbed7-f899-4361-a526-029a710d5147">SCARD_READERSTATE</a> structures that, on input, specify the readers to search and that, on output, receives the result.


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
<a href="authentication_return_values.htm">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



This service is especially useful when used in conjunction with 
<a href="https://msdn.microsoft.com/94776f3d-e8f0-4062-a766-2cf28cbfd050">SCardGetStatusChange</a>. If no matching cards are found by means of <b>SCardLocateCards</b>, the calling application may use <b>SCardGetStatusChange</b> to wait for card availability changes.

The <b>SCardLocateCards</b> function is a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> tracking function. For more information on other tracking functions, see 
<a href="https://msdn.microsoft.com/b26b26bf-85ff-435f-a679-7529f19b1c1b">Smart Card Tracking Functions</a>.

Calling this function should be done outside of a transaction. If an application begins a transaction with the <a href="https://msdn.microsoft.com/91f61060-4b0b-4890-9372-25ba0aacb642">SCardBeginTransaction</a> function and then calls this function, it resets the <i>hCard</i> parameter (of type <b>SCARDHANDLE</b>) of the <b>SCardBeginTransaction</b> function.

<b>Windows Server 2008 R2 and Windows 7:  </b>Calling this function within a transaction could result in your computer becoming unresponsive.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>Not applicable.


#### Examples

The following example  shows locating smart cards.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Copyright (C) Microsoft. All rights reserved. 
#include &lt;stdio.h&gt;
#include &lt;winscard.h&gt;
#include &lt;tchar.h&gt;
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
                                &amp;hSC );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardEstablishContext\n");
    exit(1);
}

// Determine which readers are available.
lReturn = SCardListReaders(hSC,
                           NULL,
                           (LPTSTR)&amp;szReaders,
                           &amp;cchReaders );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardListReaders\n");
    exit(1);
}
// Place the readers into the state array.
szRdr = szReaders;
for ( dwI = 0; dwI &lt; MAXIMUM_SMARTCARD_READERS; dwI++ )
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
    for ( dwI=0; dwI &lt; dwRdrCount; dwI++)
    {
        if ( 0 != ( SCARD_STATE_ATRMATCH &amp; 
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4e9bbed7-f899-4361-a526-029a710d5147">SCARD_READERSTATE</a>



<a href="https://msdn.microsoft.com/abf3b4ff-4775-40e9-b68d-97dcf6a892ba">SCardCancel</a>



<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/94776f3d-e8f0-4062-a766-2cf28cbfd050">SCardGetStatusChange</a>
 

 

