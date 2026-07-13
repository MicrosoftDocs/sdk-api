---
UID: NS:winscard.SCARD_READERSTATEA
title: SCARD_READERSTATEA (winscard.h)
description: Used by functions for tracking smart cards within readers. (ANSI)
helpviewer_keywords: ["*LPSCARD_READERSTATEA","*PSCARD_READERSTATEA","LPSCARD_READERSTATE","LPSCARD_READERSTATE structure pointer [Security]","PSCARD_READERSTATE","PSCARD_READERSTATE structure pointer [Security]","SCARD_READERSTATE","SCARD_READERSTATE structure [Security]","SCARD_READERSTATEA","SCARD_READERSTATEW","SCARD_STATE_ATRMATCH","SCARD_STATE_CHANGED","SCARD_STATE_EMPTY","SCARD_STATE_EXCLUSIVE","SCARD_STATE_IGNORE","SCARD_STATE_INUSE","SCARD_STATE_MUTE","SCARD_STATE_PRESENT","SCARD_STATE_UNAVAILABLE","SCARD_STATE_UNAWARE","SCARD_STATE_UNKNOWN","_smart_scard_readerstate","security.scard_readerstate","winscard/LPSCARD_READERSTATE","winscard/PSCARD_READERSTATE","winscard/SCARD_READERSTATE","winscard/SCARD_READERSTATEA","winscard/SCARD_READERSTATEW"]
old-location: security\scard_readerstate.htm
tech.root: security
ms.assetid: 4e9bbed7-f899-4361-a526-029a710d5147
ms.date: 12/05/2018
ms.keywords: '*LPSCARD_READERSTATEA, *PSCARD_READERSTATEA, LPSCARD_READERSTATE, LPSCARD_READERSTATE structure pointer [Security], PSCARD_READERSTATE, PSCARD_READERSTATE structure pointer [Security], SCARD_READERSTATE, SCARD_READERSTATE structure [Security], SCARD_READERSTATEA, SCARD_READERSTATEW, SCARD_STATE_ATRMATCH, SCARD_STATE_CHANGED, SCARD_STATE_EMPTY, SCARD_STATE_EXCLUSIVE, SCARD_STATE_IGNORE, SCARD_STATE_INUSE, SCARD_STATE_MUTE, SCARD_STATE_PRESENT, SCARD_STATE_UNAVAILABLE, SCARD_STATE_UNAWARE, SCARD_STATE_UNKNOWN, _smart_scard_readerstate, security.scard_readerstate, winscard/LPSCARD_READERSTATE, winscard/PSCARD_READERSTATE, winscard/SCARD_READERSTATE, winscard/SCARD_READERSTATEA, winscard/SCARD_READERSTATEW'
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCARD_READERSTATEW (Unicode) and SCARD_READERSTATEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SCARD_READERSTATEA, *PSCARD_READERSTATEA, *LPSCARD_READERSTATEA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSCARD_READERSTATEA
 - winscard/PSCARD_READERSTATEA
 - SCARD_READERSTATEA
 - winscard/SCARD_READERSTATEA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winscard.h
api_name:
 - SCARD_READERSTATE
 - SCARD_READERSTATEA
 - SCARD_READERSTATEW
---

# SCARD_READERSTATEA structure


## -description

The <b>SCARD_READERSTATE</b> structure is used by functions for tracking <a href="/windows/desktop/SecGloss/s-gly">smart cards</a> within <a href="/windows/desktop/SecGloss/r-gly">readers</a>.

## -struct-fields

### -field szReader

A pointer to the name of the reader being monitored.

Set the value of this member to "\\\\?PnP?\\Notification" and the values of all other members to zero to be notified of the arrival of a new smart card reader.

### -field pvUserData

Not used by the <a href="/windows/desktop/SecGloss/s-gly">smart card subsystem</a>. This member is used by the application.

### -field dwCurrentState

Current <a href="/windows/desktop/SecGloss/s-gly">state</a> of the reader, as seen by the application. This field can take on any of the following values, in combination, as a bitmask. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_UNAWARE"></a><a id="scard_state_unaware"></a><dl>
<dt><b>SCARD_STATE_UNAWARE</b></dt>
</dl>
</td>
<td width="60%">
The application is unaware of the current <a href="/windows/desktop/SecGloss/s-gly">state</a>, and would like to know. The use of this value results in an immediate return from state transition monitoring services. This is represented by all bits set to zero.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_IGNORE"></a><a id="scard_state_ignore"></a><dl>
<dt><b>SCARD_STATE_IGNORE</b></dt>
</dl>
</td>
<td width="60%">
The application is not interested in this reader, and it should not be considered during monitoring operations. If this bit value is set, all other bits are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_UNAVAILABLE"></a><a id="scard_state_unavailable"></a><dl>
<dt><b>SCARD_STATE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The application expects that this reader is not available for use. If this bit is set, then all the following bits are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_EMPTY"></a><a id="scard_state_empty"></a><dl>
<dt><b>SCARD_STATE_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The application expects that there is no card in the reader. If this bit is set, all the following bits are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_PRESENT"></a><a id="scard_state_present"></a><dl>
<dt><b>SCARD_STATE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The application expects that there is a card in the reader.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_ATRMATCH"></a><a id="scard_state_atrmatch"></a><dl>
<dt><b>SCARD_STATE_ATRMATCH</b></dt>
</dl>
</td>
<td width="60%">
The application expects that there is a card in the reader with an ATR that matches one of the target cards. If this bit is set, SCARD_STATE_PRESENT is assumed. This bit has no meaning to <a href="/windows/desktop/api/winscard/nf-winscard-scardgetstatuschangea">SCardGetStatusChange</a> beyond SCARD_STATE_PRESENT.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_EXCLUSIVE"></a><a id="scard_state_exclusive"></a><dl>
<dt><b>SCARD_STATE_EXCLUSIVE</b></dt>
</dl>
</td>
<td width="60%">
The application expects that the card in the reader is allocated for exclusive use by another application. If this bit is set, SCARD_STATE_PRESENT is assumed.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_INUSE"></a><a id="scard_state_inuse"></a><dl>
<dt><b>SCARD_STATE_INUSE</b></dt>
</dl>
</td>
<td width="60%">
The application expects that the card in the reader is in use by one or more other applications, but may be connected to in shared mode. If this bit is set, SCARD_STATE_PRESENT is assumed.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_MUTE"></a><a id="scard_state_mute"></a><dl>
<dt><b>SCARD_STATE_MUTE</b></dt>
</dl>
</td>
<td width="60%">
The application expects that there is an unresponsive card in the reader.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_UNPOWERED"></a><a id="scard_state_unpowered"></a><dl>
<dt><b>SCARD_STATE_UNPOWERED</b></dt>
</dl>
</td>
<td width="60%">
This implies that the card in the reader has not been powered up.

</td>
</tr>	

</table>

### -field dwEventState

Current <a href="/windows/desktop/SecGloss/s-gly">state</a> of the <a href="/windows/desktop/SecGloss/r-gly">reader</a>, as known by the <a href="/windows/desktop/SecGloss/s-gly">smart card </a><a href="/windows/desktop/SecGloss/r-gly">resource manager</a>. This field can take on any of the following values, in combination, as a bitmask. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_IGNORE"></a><a id="scard_state_ignore"></a><dl>
<dt><b>SCARD_STATE_IGNORE</b></dt>
</dl>
</td>
<td width="60%">
This reader should be ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_CHANGED"></a><a id="scard_state_changed"></a><dl>
<dt><b>SCARD_STATE_CHANGED</b></dt>
</dl>
</td>
<td width="60%">
There is a difference between the state believed by the application, and the state known by the resource manager. When this bit is set, the application may assume a significant state change has occurred on this reader.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_UNKNOWN"></a><a id="scard_state_unknown"></a><dl>
<dt><b>SCARD_STATE_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The given reader name is not recognized by the resource manager. If this bit is set, then SCARD_STATE_CHANGED and SCARD_STATE_IGNORE will also be set.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_UNAVAILABLE"></a><a id="scard_state_unavailable"></a><dl>
<dt><b>SCARD_STATE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The actual state of this reader is not available. If this bit is set, then all the following bits are clear.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_EMPTY"></a><a id="scard_state_empty"></a><dl>
<dt><b>SCARD_STATE_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
There is no card in the reader. If this bit is set, all the following bits will be clear.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_PRESENT"></a><a id="scard_state_present"></a><dl>
<dt><b>SCARD_STATE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
There is a card in the reader.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_ATRMATCH"></a><a id="scard_state_atrmatch"></a><dl>
<dt><b>SCARD_STATE_ATRMATCH</b></dt>
</dl>
</td>
<td width="60%">
There is a card in the reader with an ATR matching one of the target cards. If this bit is set, SCARD_STATE_PRESENT will also be set. This bit is only returned on the <a href="/windows/desktop/api/winscard/nf-winscard-scardlocatecardsa">SCardLocateCards</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_EXCLUSIVE"></a><a id="scard_state_exclusive"></a><dl>
<dt><b>SCARD_STATE_EXCLUSIVE</b></dt>
</dl>
</td>
<td width="60%">
The card in the reader is allocated for exclusive use by another application. If this bit is set, SCARD_STATE_PRESENT will also be set.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_INUSE"></a><a id="scard_state_inuse"></a><dl>
<dt><b>SCARD_STATE_INUSE</b></dt>
</dl>
</td>
<td width="60%">
The card in the reader is in use by one or more other applications, but may be connected to in shared mode. If this bit is set, SCARD_STATE_PRESENT will also be set.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_MUTE"></a><a id="scard_state_mute"></a><dl>
<dt><b>SCARD_STATE_MUTE</b></dt>
</dl>
</td>
<td width="60%">
There is an unresponsive card in the reader.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_STATE_UNPOWERED"></a><a id="scard_state_unpowered"></a><dl>
<dt><b>SCARD_STATE_UNPOWERED</b></dt>
</dl>
</td>
<td width="60%">
This implies that the card in the reader has not been powered up.

</td>
</tr>
</table>

### -field cbAtr

Number of bytes in the returned ATR.

### -field rgbAtr

ATR of the inserted card, with extra alignment bytes.

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardgetstatuschangea">SCardGetStatusChange</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlocatecardsa">SCardLocateCards</a>

## -remarks

> [!NOTE]
> The winscard.h header defines SCARD_READERSTATE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

