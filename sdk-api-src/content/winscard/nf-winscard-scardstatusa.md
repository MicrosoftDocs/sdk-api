---
UID: NF:winscard.SCardStatusA
title: SCardStatusA function (winscard.h)
description: Provides the current status of a smart card in a reader. (ANSI)
helpviewer_keywords: ["SCARD_ABSENT", "SCARD_NEGOTIABLE", "SCARD_POWERED", "SCARD_PRESENT", "SCARD_PROTOCOL_RAW", "SCARD_PROTOCOL_T0", "SCARD_PROTOCOL_T1", "SCARD_SPECIFIC", "SCARD_SWALLOWED", "SCardStatusA", "winscard/SCardStatusA"]
old-location: security\scardstatus.htm
tech.root: security
ms.assetid: 04547cd1-7755-4332-8195-924b803d9a84
ms.date: 12/05/2018
ms.keywords: SCARD_ABSENT, SCARD_NEGOTIABLE, SCARD_POWERED, SCARD_PRESENT, SCARD_PROTOCOL_RAW, SCARD_PROTOCOL_T0, SCARD_PROTOCOL_T1, SCARD_SPECIFIC, SCARD_SWALLOWED, SCardStatus, SCardStatus function [Security], SCardStatusA, SCardStatusW, _smart_scardstatus, security.scardstatus, winscard/SCardStatus, winscard/SCardStatusA, winscard/SCardStatusW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardStatusW (Unicode) and SCardStatusA (ANSI)
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
 - SCardStatusA
 - winscard/SCardStatusA
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
 - SCardStatus
 - SCardStatusA
 - SCardStatusW
---

# SCardStatusA function


## -description

The <b>SCardStatus</b> function provides the current status of a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> in a <a href="/windows/desktop/SecGloss/r-gly">reader</a>. You can call it any time after a successful call to <a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a> and before a successful call to <a href="/windows/desktop/api/winscard/nf-winscard-scarddisconnect">SCardDisconnect</a>. It does not affect the <a href="/windows/desktop/SecGloss/s-gly">state</a> of the reader or <a href="/windows/desktop/SecGloss/r-gly">reader driver</a>.

## -parameters

### -param hCard [in]

Reference value returned from 
<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>.

### -param mszReaderNames [out]

List of display names (multiple string) by which the currently connected reader is known.

### -param pcchReaderLen [in, out, optional]

On input, supplies the length of the <i>szReaderName</i> buffer. 




On output, receives the actual length (in characters) of the reader name list, including the trailing <b>NULL</b> character. If this buffer length is specified as SCARD_AUTOALLOCATE, then <i>szReaderName</i> is converted to a pointer to a byte pointer, and it receives the address of a block of memory that contains the multiple-string structure.

### -param pdwState [out, optional]

Current <a href="/windows/desktop/SecGloss/s-gly">state</a> of the smart card in the reader. Upon success, it receives one of the following state indicators. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_ABSENT"></a><a id="scard_absent"></a><dl>
<dt><b>SCARD_ABSENT</b></dt>
</dl>
</td>
<td width="60%">
There is no card in the reader.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PRESENT"></a><a id="scard_present"></a><dl>
<dt><b>SCARD_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
There is a card in the reader, but it has not been moved into position for use.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_SWALLOWED"></a><a id="scard_swallowed"></a><dl>
<dt><b>SCARD_SWALLOWED</b></dt>
</dl>
</td>
<td width="60%">
There is a card in the reader in position for use. The card is not powered.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_POWERED"></a><a id="scard_powered"></a><dl>
<dt><b>SCARD_POWERED</b></dt>
</dl>
</td>
<td width="60%">
Power is being provided to the card, but the reader driver is unaware of the mode of the card.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_NEGOTIABLE"></a><a id="scard_negotiable"></a><dl>
<dt><b>SCARD_NEGOTIABLE</b></dt>
</dl>
</td>
<td width="60%">
The card has been reset and is awaiting PTS negotiation.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_SPECIFIC"></a><a id="scard_specific"></a><dl>
<dt><b>SCARD_SPECIFIC</b></dt>
</dl>
</td>
<td width="60%">
The card has been reset and specific <a href="/windows/desktop/SecGloss/c-gly">communication protocols</a> have been established.

</td>
</tr>
</table>

### -param pdwProtocol [out, optional]

Current protocol, if any. The returned value is meaningful only if the returned value of <i>pdwState</i> is SCARD_SPECIFICMODE.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROTOCOL_RAW"></a><a id="scard_protocol_raw"></a><dl>
<dt><b>SCARD_PROTOCOL_RAW</b></dt>
</dl>
</td>
<td width="60%">
The Raw Transfer protocol is in use.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROTOCOL_T0"></a><a id="scard_protocol_t0"></a><dl>
<dt><b>SCARD_PROTOCOL_T0</b></dt>
</dl>
</td>
<td width="60%">
The ISO 7816/3 <a href="/windows/desktop/SecGloss/t-gly">T=0</a> protocol is in use.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROTOCOL_T1"></a><a id="scard_protocol_t1"></a><dl>
<dt><b>SCARD_PROTOCOL_T1</b></dt>
</dl>
</td>
<td width="60%">
The ISO 7816/3 <a href="/windows/desktop/SecGloss/t-gly">T=1</a> protocol is in use.

</td>
</tr>
</table>

### -param pbAtr [out]

Pointer to a 32-byte buffer that receives the <a href="/windows/desktop/SecGloss/a-gly">ATR string</a> from the currently inserted card, if available.

### -param pcbAtrLen [in, out, optional]

On input, supplies the length of the <i>pbAtr</i> buffer. On output, receives the number of bytes in the ATR string (32 bytes maximum). If this buffer length is specified as SCARD_AUTOALLOCATE, then <i>pbAtr</i> is converted to a pointer to a byte pointer, and it receives the address of a block of memory that contains the multiple-string structure.

## -returns

If the function successfully provides the current status of a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> in a <a href="/windows/desktop/SecGloss/r-gly">reader</a>, the return value is SCARD_S_SUCCESS.

If the function fails, it returns an error code. For more information, see 
<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

## -remarks

The <b>SCardStatus</b> function is a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> and <a href="/windows/desktop/SecGloss/r-gly">reader</a> access function. For information about other access functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-and-reader-access-functions">Smart Card and Reader Access Functions</a>.


#### Examples

The following example  shows how to determine the state of the smart card.


```cpp
WCHAR           szReader[200];
DWORD           cch = 200;
BYTE            bAttr[32];
DWORD           cByte = 32;
DWORD           dwState, dwProtocol;
LONG            lReturn;

// Determine the status.
// hCardHandle was set by an earlier call to SCardConnect.
lReturn = SCardStatus(hCardHandle,
                      szReader,
                      &cch,
                      &dwState,
                      &dwProtocol,
                      (LPBYTE)&bAttr,
                      &cByte); 

if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardStatus\n");
    exit(1);     // or other appropriate action
}

// Examine retrieved status elements.
// Look at the reader name and card state.
printf("%S\n", szReader );
switch ( dwState )
{
    case SCARD_ABSENT:
        printf("Card absent.\n");
        break;
    case SCARD_PRESENT:
        printf("Card present.\n");
        break;
    case SCARD_SWALLOWED:
        printf("Card swallowed.\n");
        break;
    case SCARD_POWERED:
        printf("Card has power.\n");
        break;
    case SCARD_NEGOTIABLE:
        printf("Card reset and waiting PTS negotiation.\n");
        break;
    case SCARD_SPECIFIC:
        printf("Card has specific communication protocols set.\n");
        break;
    default:
        printf("Unknown or unexpected card state.\n");
        break;
}

```






> [!NOTE]
> The winscard.h header defines SCardStatus as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scarddisconnect">SCardDisconnect</a>
