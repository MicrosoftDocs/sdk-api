---
UID: NF:winscard.SCardBeginTransaction
title: SCardBeginTransaction function
author: windows-sdk-content
description: Starts a transaction.
old-location: security\scardbegintransaction.htm
tech.root: SecAuthN
ms.assetid: 91f61060-4b0b-4890-9372-25ba0aacb642
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SCardBeginTransaction, SCardBeginTransaction function [Security], _smart_scardbegintransaction, security.scardbegintransaction, winscard/SCardBeginTransaction
ms.topic: function
req.header: winscard.h
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
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardBeginTransaction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SCardBeginTransaction function


## -description


The <b>SCardBeginTransaction</b> function starts a <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">transaction</a>.

 The function waits for the completion of all other transactions before it begins. After the transaction starts, all other applications are blocked from accessing the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> while the transaction is in progress.


## -parameters




### -param hCard [in]

A reference value obtained from a previous call to 
<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>.


## -returns



If the function succeeds, it returns <b>SCARD_S_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa374738(v=VS.85).aspx">Smart Card Return Values</a>.

If another process or thread has reset the card, SCARD_W_RESET_CARD is returned as expected.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This function returns <b>SCARD_S_SUCCESS</b> even if another process or thread has reset the card. To determine whether the card has been reset, call the <a href="https://msdn.microsoft.com/04547cd1-7755-4332-8195-924b803d9a84">SCardStatus</a> function immediately after calling this function.




## -remarks



If a transaction is held on the card for more than five seconds with no operations happening on that card, then the card is reset. Calling any of the <a href="https://msdn.microsoft.com/37d92491-174b-471e-b36e-46d9285dd404">Smart Card and Reader Access Functions</a> or <a href="https://msdn.microsoft.com/ea6cfa5a-2abf-4b7f-b3f4-99655266f030">Direct Card Access Functions</a> on the card that is transacted results in the timer being reset to continue allowing the transaction to be used.

The <b>SCardBeginTransaction</b> function is a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> and <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a> access function. For more information about other access functions, see 
<a href="https://msdn.microsoft.com/37d92491-174b-471e-b36e-46d9285dd404">Smart Card and Reader Access Functions</a>.


#### Examples

The following example demonstrates how to begin a smart card transaction. The example assumes that <code>lReturn</code> is an existing variable of type <b>LONG</b> and that <code>hCard</code> is a valid handle received from a previous call to <a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>.


```cpp

lReturn = SCardBeginTransaction( hCard );
if ( SCARD_S_SUCCESS != lReturn )
 printf("Failed SCardBeginTransaction\n");

```





## -see-also




<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>



<a href="https://msdn.microsoft.com/0acaff20-006a-47d3-bc7a-834b3281cde6">SCardEndTransaction</a>
 

 

