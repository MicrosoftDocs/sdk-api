---
UID: NF:winscard.SCardDisconnect
title: SCardDisconnect function (winscard.h)
description: Terminates a connection previously opened between the calling application and a smart card in the target reader.
helpviewer_keywords: ["SCARD_EJECT_CARD","SCARD_LEAVE_CARD","SCARD_RESET_CARD","SCARD_UNPOWER_CARD","SCardDisconnect","SCardDisconnect function [Security]","_smart_scarddisconnect","security.scarddisconnect","winscard/SCardDisconnect"]
old-location: security\scarddisconnect.htm
tech.root: security
ms.assetid: d087a006-bd2d-4ad7-965b-36ea8d712ec8
ms.date: 12/05/2018
ms.keywords: SCARD_EJECT_CARD, SCARD_LEAVE_CARD, SCARD_RESET_CARD, SCARD_UNPOWER_CARD, SCardDisconnect, SCardDisconnect function [Security], _smart_scarddisconnect, security.scarddisconnect, winscard/SCardDisconnect
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
 - SCardDisconnect
 - winscard/SCardDisconnect
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
 - Ext-MS-Win-wlan-scard-l1-1-0.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardDisconnect
---

# SCardDisconnect function


## -description

The <b>SCardDisconnect</b> function terminates a connection previously opened between the calling application and a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> in the target <a href="/windows/desktop/SecGloss/r-gly">reader</a>.

## -parameters

### -param hCard [in]

Reference value obtained from a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>.

### -param dwDisposition [in]

Action to take on the card in the connected reader on close. 
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<tr>
<td width="40%"><a id="SCARD_EJECT_CARD"></a><a id="scard_eject_card"></a><dl>
<dt><b>SCARD_EJECT_CARD</b></dt>
</dl>
</td>
<td width="60%">
Eject the card.

</td>
</tr>
</table>

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

If an application (which previously called 
<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>) exits without calling <b>SCardDisconnect</b>, the card is automatically reset.

The <b>SCardDisconnect</b> function is a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> and <a href="/windows/desktop/SecGloss/r-gly">reader</a> access function. For more information on other access functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-and-reader-access-functions">Smart Card and Reader Access Functions</a>.


#### Examples

The following example terminates the specified smart card connection. The example assumes that lReturn is a variable of type <b>LONG</b>, and that hCardHandle is a valid handle received from a previous call to <a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>.


```cpp

lReturn = SCardDisconnect(hCardHandle, 
                          SCARD_LEAVE_CARD);
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardDisconnect\n");
    exit(1);  // Or other appropriate action.
}

```

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardreconnect">SCardReconnect</a>