---
UID: NF:winscard.SCardTransmit
title: SCardTransmit function (winscard.h)
description: Sends a service request to the smart card and expects to receive data back from the card.
helpviewer_keywords: ["SCardTransmit","SCardTransmit function [Security]","_smart_scardtransmit","bCla","bIns","bP1","bP2","bP3","security.scardtransmit","winscard/SCardTransmit"]
old-location: security\scardtransmit.htm
tech.root: security
ms.assetid: d0c16b67-34e7-4872-aa36-79dcad19093e
ms.date: 12/05/2018
ms.keywords: SCardTransmit, SCardTransmit function [Security], _smart_scardtransmit, bCla, bIns, bP1,bP2, bP3, security.scardtransmit, winscard/SCardTransmit
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
 - SCardTransmit
 - winscard/SCardTransmit
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
 - SCardTransmit
---

# SCardTransmit function


## -description

The <b>SCardTransmit</b> function sends a service request to the <a href="/windows/desktop/SecGloss/s-gly">smart card</a> and expects to receive data back from the card.

## -parameters

### -param hCard [in]

A reference value returned from 
the <a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a> function.

### -param pioSendPci [in]

A pointer to the protocol header structure for the instruction. This buffer is in the format of an <a href="/windows/desktop/SecAuthN/scard-io-request">SCARD_IO_REQUEST</a> structure, followed by the specific protocol control information (PCI). 




For the <a href="/windows/desktop/SecGloss/t-gly">T=0</a>, <a href="/windows/desktop/SecGloss/t-gly">T=1</a>, and Raw protocols, the PCI structure is constant. The <a href="/windows/desktop/SecGloss/s-gly">smart card subsystem</a> supplies a global T=0, T=1, or Raw PCI structure, which you can reference by using the symbols SCARD_PCI_T0, SCARD_PCI_T1, and SCARD_PCI_RAW respectively.

### -param pbSendBuffer [in]

A pointer to the actual data to be written to the card. 

For T=0, the data parameters are placed into the address pointed to by <i>pbSendBuffer</i> according to the following structure:


```cpp
struct {
    BYTE
        bCla,   // the instruction class
        bIns,   // the instruction code 
        bP1,    // parameter to the instruction
        bP2,    // parameter to the instruction
        bP3;    // size of I/O transfer
} CmdBytes;

```



The data sent to the card should immediately follow the send buffer. In the special case where no data is sent to the card and no data is expected in return, <b>bP3</b> is not sent.



<table>
<tr>
<th>Member</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="bCla"></a><a id="bcla"></a><a id="BCLA"></a><dl>
<dt><b><b>bCla</b></b></dt>
</dl>
</td>
<td width="60%">
The T=0 instruction class.

</td>
</tr>
<tr>
<td width="40%"><a id="bIns"></a><a id="bins"></a><a id="BINS"></a><dl>
<dt><b><b>bIns</b></b></dt>
</dl>
</td>
<td width="60%">
An instruction code in the T=0 instruction class.

</td>
</tr>
<tr>
<td width="40%"><a id="bP1__bP2"></a><a id="bp1__bp2"></a><a id="BP1__BP2"></a><dl>
<dt><b><b>bP1</b>, <b>bP2</b></b></dt>
</dl>
</td>
<td width="60%">
Reference codes that complete the instruction code.

</td>
</tr>
<tr>
<td width="40%"><a id="bP3"></a><a id="bp3"></a><a id="BP3"></a><dl>
<dt><b><b>bP3</b></b></dt>
</dl>
</td>
<td width="60%">
The number of data bytes to be transmitted during the command, per ISO 7816-4, Section 8.2.1.

</td>
</tr>
</table>

### -param cbSendLength [in]

The length, in bytes, of the <i>pbSendBuffer</i> parameter. 




For T=0, in the special case where no data is sent to the card and no data expected in return, this length must reflect that the <b>bP3</b> member is not being sent; the length should be <code>sizeof(CmdBytes)  - sizeof(BYTE)</code>.

### -param pioRecvPci [in, out, optional]

Pointer to the protocol header structure for the instruction, followed by a buffer in which to receive any returned protocol control information (PCI) specific to the protocol in use. This parameter can be <b>NULL</b> if no  PCI is returned.

### -param pbRecvBuffer [out]

Pointer to any data returned from the card. 




For T=0, the data is immediately followed by the SW1 and SW2 status bytes. If no data is returned from the card, then this buffer will only contain the SW1 and SW2 status bytes.

### -param pcbRecvLength [in, out]

Supplies the length, in bytes, of the <i>pbRecvBuffer</i> parameter and receives the actual number of bytes received from the smart card. 


This value cannot be SCARD_AUTOALLOCATE because <b>SCardTransmit</b> does not support SCARD_AUTOALLOCATE.

For T=0, the receive buffer must be at least two bytes long to receive the SW1 and SW2 status bytes.

## -returns

If the function successfully sends a service request to the <a href="/windows/desktop/SecGloss/s-gly">smart card</a>, the return value is SCARD_S_SUCCESS.

If the function fails, it returns an error code. For more information, see 
<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

## -remarks

The <b>SCardTransmit</b> function is a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> and <a href="/windows/desktop/SecGloss/r-gly">reader</a> access function. For information about other access functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-and-reader-access-functions">Smart Card and Reader Access Functions</a>.

For the <a href="/windows/desktop/SecGloss/t-gly">T=0 protocol</a>, the data received back are the SW1 and SW2 status codes, possibly preceded by response data. The following paragraphs provide information about the send and receive buffers used to transfer data and issue a command.




#### Examples

The following example  shows sending a service request to the smart card.


```cpp
//  Transmit the request.
//  lReturn is of type LONG.
//  hCardHandle was set by a previous call to SCardConnect.
//  pbSend points to the buffer of bytes to send.
//  dwSend is the DWORD value for the number of bytes to send.
//  pbRecv points to the buffer for returned bytes.
//  dwRecv is the DWORD value for the number of returned bytes.
lReturn = SCardTransmit(hCardHandle,
                        SCARD_PCI_T0,
                        pbSend,
                        dwSend,
                        NULL,
                        pbRecv,
                        &dwRecv );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardTransmit\n");
    exit(1);   // or other appropriate error action
}

```

## -see-also

<a href="/windows/desktop/SecAuthN/scard-io-request">SCARD_IO_REQUEST</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>