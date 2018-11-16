---
UID: NF:winscard.SCardStatusW
title: SCardStatusW function
author: windows-sdk-content
description: Provides the current status of a smart card in a reader.
old-location: security\scardstatus.htm
tech.root: SecAuthN
ms.assetid: 04547cd1-7755-4332-8195-924b803d9a84
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SCARD_ABSENT, SCARD_NEGOTIABLE, SCARD_POWERED, SCARD_PRESENT, SCARD_PROTOCOL_RAW, SCARD_PROTOCOL_T0, SCARD_PROTOCOL_T1, SCARD_SPECIFIC, SCARD_SWALLOWED, SCardStatus, SCardStatus function [Security], SCardStatusA, SCardStatusW, _smart_scardstatus, security.scardstatus, winscard/SCardStatus, winscard/SCardStatusA, winscard/SCardStatusW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SCardStatusW
: 
---

# SCardStatusW function


## -description


The <b>SCardStatus</b> function provides the current status of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> in a <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a>. You can call it any time after a successful call to <a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a> and before a successful call to <a href="https://msdn.microsoft.com/d087a006-bd2d-4ad7-965b-36ea8d712ec8">SCardDisconnect</a>. It does not affect the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a> of the reader or <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader driver</a>.


## -parameters




### -param hCard [in]

Reference value returned from 
<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>.


### -param mszReaderNames [out]

List of display names (multiple string) by which the currently connected reader is known.


### -param pcchReaderLen [in, out, optional]

On input, supplies the length of the <i>szReaderName</i> buffer. 




On output, receives the actual length (in characters) of the reader name list, including the trailing <b>NULL</b> character. If this buffer length is specified as SCARD_AUTOALLOCATE, then <i>szReaderName</i> is converted to a pointer to a byte pointer, and it receives the address of a block of memory that contains the multiple-string structure.


### -param pdwState [out, optional]

Current <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a> of the smart card in the reader. Upon success, it receives one of the following state indicators. 




					

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
The card has been reset and specific <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">communication protocols</a> have been established.

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
The ISO 7816/3 <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">T=0</a> protocol is in use.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_PROTOCOL_T1"></a><a id="scard_protocol_t1"></a><dl>
<dt><b>SCARD_PROTOCOL_T1</b></dt>
</dl>
</td>
<td width="60%">
The ISO 7816/3 <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">T=1</a> protocol is in use.

</td>
</tr>
</table>
 


### -param pbAtr [out]

Pointer to a 32-byte buffer that receives the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ATR string</a> from the currently inserted card, if available.


### -param pcbAtrLen [in, out, optional]

On input, supplies the length of the <i>pbAtr</i> buffer. On output, receives the number of bytes in the ATR string (32 bytes maximum). If this buffer length is specified as SCARD_AUTOALLOCATE, then <i>pbAtr</i> is converted to a pointer to a byte pointer, and it receives the address of a block of memory that contains the multiple-string structure.


## -returns



If the function successfully provides the current status of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> in a <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a>, the return value is SCARD_S_SUCCESS.

If the function fails, it returns an error code. For more information, see 
<a href="authentication_return_values.htm">Smart Card Return Values</a>.




## -remarks



The <b>SCardStatus</b> function is a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> and <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a> access function. For information about other access functions, see 
<a href="https://msdn.microsoft.com/37d92491-174b-471e-b36e-46d9285dd404">Smart Card and Reader Access Functions</a>.


#### Examples

The following example  shows how to determine the state of the smart card.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>WCHAR           szReader[200];
DWORD           cch = 200;
BYTE            bAttr[32];
DWORD           cByte = 32;
DWORD           dwState, dwProtocol;
LONG            lReturn;

// Determine the status.
// hCardHandle was set by an earlier call to SCardConnect.
lReturn = SCardStatus(hCardHandle,
                      szReader,
                      &amp;cch,
                      &amp;dwState,
                      &amp;dwProtocol,
                      (LPBYTE)&amp;bAttr,
                      &amp;cByte); 

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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>



<a href="https://msdn.microsoft.com/d087a006-bd2d-4ad7-965b-36ea8d712ec8">SCardDisconnect</a>
 

 

