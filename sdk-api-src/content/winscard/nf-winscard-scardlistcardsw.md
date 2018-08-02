---
UID: NF:winscard.SCardListCardsW
title: SCardListCardsW function
author: windows-sdk-content
description: Searches the smart card database and provides a list of named cards previously introduced to the system by the user.
old-location: security\scardlistcards.htm
old-project: SecAuthN
ms.assetid: b8ecbb8c-e1fb-485b-9a2c-20e6edf25cf1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SCardListCards, SCardListCards function [Security], SCardListCardsA, SCardListCardsW, _smart_scardlistcards, security.scardlistcards, winscard/SCardListCards, winscard/SCardListCardsA, winscard/SCardListCardsW
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
req.unicode-ansi: SCardListCardsW (Unicode) and SCardListCardsA (ANSI)
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
 - SCardListCards
 - SCardListCardsA
 - SCardListCardsW
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardListCardsW function


## -description


The <b>SCardListCards</b> function searches the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card database</a> and provides a list of named cards previously introduced to the system by the user.

The caller specifies an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ATR string</a>, a set of interface identifiers (GUIDs), or both. If both an ATR string and an identifier array are supplied, the cards returned will match the ATR string supplied and support the interfaces specified.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a> for the query. The resource manager context can be set by a previous call to <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>.

If this parameter is set to <b>NULL</b>, the search for cards is not limited to any context.


### -param pbAtr [in, optional]

Address of an ATR string to compare to known cards, or <b>NULL</b> if no ATR matching is to be performed.


### -param rgquidInterfaces

TBD


### -param cguidInterfaceCount [in]

Number of entries in the <i>rgguidInterfaces</i> array. If <i>rgguidInterfaces</i> is <b>NULL</b>, then this value is ignored.


### -param mszCards [out]

Multi-string that lists the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart cards</a> found. If this value is <b>NULL</b>, <b>SCardListCards</b> ignores the buffer length supplied in <i>pcchCards</i>, returning the length of the buffer that would have been returned if this parameter had not been <b>NULL</b> to <i>pcchCards</i> and a success code.


### -param pcchCards [in, out]

Length of the <i>mszCards</i> buffer in characters. Receives the actual length of the multi-string structure, including all trailing <b>null</b> characters. If the buffer length is specified as SCARD_AUTOALLOCATE, then <i>mszCards</i> is converted to a pointer to a byte pointer, and receives the address of a block of memory containing the multi-string structure. This block of memory must be deallocated with 
<a href="https://msdn.microsoft.com/d41d3891-671b-4129-8034-b251af983830">SCardFreeMemory</a>.


#### - rgguidInterfaces [in]

Array of identifiers (GUIDs), or <b>NULL</b> if no interface matching is to be performed. When an array is supplied, a card name will be returned only if all the specified identifiers are supported by the card.


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
<a href="https://msdn.microsoft.com/en-us/library/Aa374738(v=VS.85).aspx">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



This function is not redirected, but calling the function when inside a Remote Desktop session  will not result in an error. It only means that the result will be from the remote computer instead of the local computer. 

To return all smart cards introduced to the subsystem, set <i>pbAtr</i> and <i>rgguidInterfaces</i> to <b>NULL</b>.

The <b>SCardListCards</b> function is a database query function. For more information on other database query functions, see 
<a href="https://msdn.microsoft.com/a30cbb99-522c-4752-bfcd-75be608785f1">Smart Card Database Query Functions</a>.

Calling this function should be done outside of a transaction. If an application begins a transaction with the <a href="https://msdn.microsoft.com/91f61060-4b0b-4890-9372-25ba0aacb642">SCardBeginTransaction</a> function and then calls this function, it resets the <i>hCard</i> parameter (of type <b>SCARDHANDLE</b>) of the <b>SCardBeginTransaction</b> function.

<b>Windows Server 2008 R2 and Windows 7:  </b>Calling this function within a transaction could result in your computer becoming unresponsive.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>Not applicable.


#### Examples

The following example  shows listing of the smart cards.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LPTSTR pmszCards = NULL;
LPTSTR pCard;
LONG lReturn;
DWORD cch = SCARD_AUTOALLOCATE;

// Retrieve the list of cards.
lReturn = SCardListCards(NULL,
                         NULL,
                         NULL,
                         NULL,
                         (LPTSTR)&amp;pmszCards,
                         &amp;cch );
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/d41d3891-671b-4129-8034-b251af983830">SCardFreeMemory</a>



<a href="https://msdn.microsoft.com/6e0f42af-9ac1-469b-b241-939d64676d99">SCardGetProviderId</a>



<a href="https://msdn.microsoft.com/2460c133-3ad4-4f73-9f55-56fc3bab9cdb">SCardListInterfaces</a>



<a href="https://msdn.microsoft.com/df01fa4b-8053-4d3a-ae2e-66eeb6583225">SCardListReaderGroups</a>



<a href="https://msdn.microsoft.com/b50218f1-e960-4838-b44b-6c71fa94a0ad">SCardListReaders</a>
 

 

