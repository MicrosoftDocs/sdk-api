---
UID: NF:winscard.SCardBeginTransaction
title: SCardBeginTransaction function (winscard.h)
description: Starts a transaction.
helpviewer_keywords: ["SCardBeginTransaction","SCardBeginTransaction function [Security]","_smart_scardbegintransaction","security.scardbegintransaction","winscard/SCardBeginTransaction"]
old-location: security\scardbegintransaction.htm
tech.root: security
ms.assetid: 91f61060-4b0b-4890-9372-25ba0aacb642
ms.date: 12/05/2018
ms.keywords: SCardBeginTransaction, SCardBeginTransaction function [Security], _smart_scardbegintransaction, security.scardbegintransaction, winscard/SCardBeginTransaction
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardBeginTransaction
 - winscard/SCardBeginTransaction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-security-winscard-l1-1-1.dll
 - Winscard.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardBeginTransaction
---

# SCardBeginTransaction function


## -description

The <b>SCardBeginTransaction</b> function starts a <a href="/windows/desktop/SecGloss/t-gly">transaction</a>.

 The function waits for the completion of all other transactions before it begins. After the transaction starts, all other applications are blocked from accessing the <a href="/windows/desktop/SecGloss/s-gly">smart card</a> while the transaction is in progress.

## -parameters

### -param hCard [in]

A reference value obtained from a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>.

## -returns

If the function succeeds, it returns <b>SCARD_S_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see <a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

If another process or thread has reset the card, SCARD_W_RESET_CARD is returned as expected.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This function returns <b>SCARD_S_SUCCESS</b> even if another process or thread has reset the card. To determine whether the card has been reset, call the <a href="/windows/desktop/api/winscard/nf-winscard-scardstatusa">SCardStatus</a> function immediately after calling this function.

## -remarks

If a transaction is held on the card for more than five seconds with no operations happening on that card, then the card is reset. Calling any of the <a href="/windows/desktop/SecAuthN/smart-card-and-reader-access-functions">Smart Card and Reader Access Functions</a> or <a href="/windows/desktop/SecAuthN/direct-card-access-functions">Direct Card Access Functions</a> on the card that is transacted results in the timer being reset to continue allowing the transaction to be used.

The <b>SCardBeginTransaction</b> function is a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> and <a href="/windows/desktop/SecGloss/r-gly">reader</a> access function. For more information about other access functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-and-reader-access-functions">Smart Card and Reader Access Functions</a>.


#### Examples

The following example demonstrates how to begin a smart card transaction. The example assumes that <code>lReturn</code> is an existing variable of type <b>LONG</b> and that <code>hCard</code> is a valid handle received from a previous call to <a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>.


```cpp

lReturn = SCardBeginTransaction( hCard );
if ( SCARD_S_SUCCESS != lReturn )
 printf("Failed SCardBeginTransaction\n");

```

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardendtransaction">SCardEndTransaction</a>