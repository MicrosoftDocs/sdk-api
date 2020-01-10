---
UID: NF:winscard.SCardLocateCardsByATRA
title: SCardLocateCardsByATRA function (winscard.h)
description: Searches the readers listed in the rgReaderStates parameter for a card with a name that matches one of the card names contained in one of the SCARD_ATRMASK structures specified by the rgAtrMasks parameter.
old-location: security\scardlocatecardsbyatr.htm
tech.root: SecAuthN
ms.assetid: 6c4a644c-033f-4654-b96d-0379e9ac0bb4
ms.date: 12/05/2018
ms.keywords: SCardLocateCardsByATR, SCardLocateCardsByATR function [Security], SCardLocateCardsByATRA, SCardLocateCardsByATRW, _smart_scardlocatecardsbyatr, security.scardlocatecardsbyatr, winscard/SCardLocateCardsByATR, winscard/SCardLocateCardsByATRA, winscard/SCardLocateCardsByATRW
f1_keywords:
- winscard/SCardLocateCardsByATR
dev_langs:
- c++
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardLocateCardsByATRW (Unicode) and SCardLocateCardsByATRA (ANSI)
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
- SCardLocateCardsByATR
- SCardLocateCardsByATRA
- SCardLocateCardsByATRW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SCardLocateCardsByATRA function


## -description


The <b>SCardLocateCardsByATR</b> function searches the readers listed in the <i>rgReaderStates</i> parameter for a card with a name that matches one of the card names contained in one of the <a href="https://docs.microsoft.com/windows/desktop/api/winscard/ns-winscard-scard_atrmask">SCARD_ATRMASK</a> structures specified by the <i>rgAtrMasks</i> parameter.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>.


### -param rgAtrMasks [in]

Array of 
<a href="https://docs.microsoft.com/windows/desktop/api/winscard/ns-winscard-scard_atrmask">SCARD_ATRMASK</a> structures that contain the names of the cards for which to search.


### -param cAtrs [in]

Number of elements in the <i>rgAtrMasks</i> array.
					


### -param rgReaderStates [in, out]

Array of <a href="https://docs.microsoft.com/windows/desktop/api/winscard/ns-winscard-scard_readerstatea">SCARD_READERSTATE</a> structures that specify the readers to search, and receive the result.


### -param cReaders [in]

Number of elements in the <i>rgReaderStates</i> array.


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
Error code. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



This service is especially useful when used in conjunction with 
<a href="https://docs.microsoft.com/windows/desktop/api/winscard/nf-winscard-scardgetstatuschangea">SCardGetStatusChange</a>. If no matching cards are found by means of <a href="https://docs.microsoft.com/windows/desktop/api/winscard/nf-winscard-scardlocatecardsa">SCardLocateCards</a>, the calling application may use <b>SCardGetStatusChange</b> to wait for card availability changes.

The <b>SCardLocateCardsByATR</b> function is a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">smart card</a> tracking function. For information about other tracking functions, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/smart-card-tracking-functions">Smart Card Tracking Functions</a>.



