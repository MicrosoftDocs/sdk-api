---
UID: NF:winscard.SCardEndTransaction
title: SCardEndTransaction function (winscard.h)
description: Completes a previously declared transaction, allowing other applications to resume interactions with the card.
helpviewer_keywords: ["SCARD_EJECT_CARD","SCARD_LEAVE_CARD","SCARD_RESET_CARD","SCARD_UNPOWER_CARD","SCardEndTransaction","SCardEndTransaction function [Security]","_smart_scardendtransaction","security.scardendtransaction","winscard/SCardEndTransaction"]
old-location: security\scardendtransaction.htm
tech.root: security
ms.assetid: 0acaff20-006a-47d3-bc7a-834b3281cde6
ms.date: 12/05/2018
ms.keywords: SCARD_EJECT_CARD, SCARD_LEAVE_CARD, SCARD_RESET_CARD, SCARD_UNPOWER_CARD, SCardEndTransaction, SCardEndTransaction function [Security], _smart_scardendtransaction, security.scardendtransaction, winscard/SCardEndTransaction
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
 - SCardEndTransaction
 - winscard/SCardEndTransaction
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
 - SCardEndTransaction
---

# SCardEndTransaction function


## -description

The <b>SCardEndTransaction</b> function completes a previously declared <a href="/windows/desktop/SecGloss/t-gly">transaction</a>, allowing other applications to resume interactions with the card.

## -parameters

### -param hCard [in]

Reference value obtained from a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>. This value would also have been used in an earlier call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardbegintransaction">SCardBeginTransaction</a>.

### -param dwDisposition [in]

Action to take on the card in the connected reader on close. 
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_EJECT_CARD"></a><a id="scard_eject_card"></a><dl>
<dt><b>SCARD_EJECT_CARD</b></dt>
</dl>
</td>
<td width="60%">
Eject the card.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_LEAVE_CARD"></a><a id="scard_leave_card"></a><dl>
<dt><b>SCARD_LEAVE_CARD</b></dt>
</dl>
</td>
<td width="60%">
Do not do anything special.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_RESET_CARD"></a><a id="scard_reset_card"></a><dl>
<dt><b>SCARD_RESET_CARD</b></dt>
</dl>
</td>
<td width="60%">
Reset the card.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_UNPOWER_CARD"></a><a id="scard_unpower_card"></a><dl>
<dt><b>SCARD_UNPOWER_CARD</b></dt>
</dl>
</td>
<td width="60%">
Power down the card.

</td>
</tr>
</table>

## -returns

If the function succeeds, the function returns <b>SCARD_S_SUCCESS</b>. 

If the function fails, it returns an error code. For more information, see <a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.   Possible error codes follow.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_W_RESET_CARD</b></dt>
<dt>0x80100068L</dt>
</dl>
</td>
<td width="60%">
The transaction was released. Any future communication with the card requires a call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardreconnect">SCardReconnect</a> function.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>The transaction was not released. The application must immediately call the <a href="/windows/desktop/api/winscard/nf-winscard-scarddisconnect">SCardDisconnect</a>, <a href="/windows/desktop/api/winscard/nf-winscard-scardreconnect">SCardReconnect</a>, or <a href="/windows/desktop/api/winscard/nf-winscard-scardreleasecontext">SCardReleaseContext</a> function to avoid an existing transaction blocking other threads and processes from communicating with the smart card.

</td>
</tr>
</table>

## -remarks

The <b>SCardEndTransaction</b> function is a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> and <a href="/windows/desktop/SecGloss/r-gly">reader</a> access function. For more information on other access functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-and-reader-access-functions">Smart Card and Reader Access Functions</a>.


#### Examples

The following example ends a smart card transaction. The example assumes that lReturn is a valid variable of type <b>LONG</b>, that hCard is a valid handle received from a previous call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a> function, and that hCard was passed to a previous call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardbegintransaction">SCardBeginTransaction</a> function.


```cpp

lReturn = SCardEndTransaction(hCard, 
                              SCARD_LEAVE_CARD);
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardEndTransaction\n");

```

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardbegintransaction">SCardBeginTransaction</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>