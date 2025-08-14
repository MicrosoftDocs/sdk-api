---
UID: NF:winscard.SCardGetStatusChangeW
title: SCardGetStatusChangeW function (winscard.h)
description: Blocks execution until the current availability of the cards in a specific set of readers changes. (Unicode)
helpviewer_keywords: ["SCardGetStatusChange", "SCardGetStatusChange function [Security]", "SCardGetStatusChangeW", "_smart_scardgetstatuschange", "security.scardgetstatuschange", "winscard/SCardGetStatusChange", "winscard/SCardGetStatusChangeW"]
old-location: security\scardgetstatuschange.htm
tech.root: security
ms.assetid: 94776f3d-e8f0-4062-a766-2cf28cbfd050
ms.date: 12/05/2018
ms.keywords: SCardGetStatusChange, SCardGetStatusChange function [Security], SCardGetStatusChangeA, SCardGetStatusChangeW, _smart_scardgetstatuschange, security.scardgetstatuschange, winscard/SCardGetStatusChange, winscard/SCardGetStatusChangeA, winscard/SCardGetStatusChangeW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardGetStatusChangeW (Unicode) and SCardGetStatusChangeA (ANSI)
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
 - SCardGetStatusChangeW
 - winscard/SCardGetStatusChangeW
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
 - SCardGetStatusChange
 - SCardGetStatusChangeA
 - SCardGetStatusChangeW
---

# SCardGetStatusChangeW function


## -description

The <b>SCardGetStatusChange</b> function blocks execution until the current availability of the cards in a specific set of readers changes.

The caller supplies a list of <a href="/windows/desktop/SecGloss/r-gly">readers</a> to be monitored by an SCARD_READERSTATE array and the maximum amount of time (in milliseconds) that it is willing to wait for an action to occur on one of the listed readers. Note that <b>SCardGetStatusChange</b> uses the user-supplied value in the <b>dwCurrentState</b> members of the <i>rgReaderStates</i><a href="/windows/desktop/api/winscard/ns-winscard-scard_readerstatea">SCARD_READERSTATE</a> array as the definition of the current <a href="/windows/desktop/SecGloss/s-gly">state</a> of the readers. The function returns when there is a change in availability, having filled in the <b>dwEventState</b> members of <i>rgReaderStates</i> appropriately.

## -parameters

### -param hContext [in]

A handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
the <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> function.

### -param dwTimeout [in]

The maximum amount of time, in milliseconds, to wait for an action. A value of zero causes the function to return immediately. A value of INFINITE causes this function never to time out.

### -param rgReaderStates [in, out]

An array of 
<a href="/windows/desktop/api/winscard/ns-winscard-scard_readerstatea">SCARD_READERSTATE</a> structures that specify the readers to watch, and that receives the result.

To be notified of the arrival of a new smart card reader, set the <b>szReader</b> member of a <a href="/windows/desktop/api/winscard/ns-winscard-scard_readerstatea">SCARD_READERSTATE</a> structure to "\\\\?PnP?\\Notification", and set all of the other members of that structure to zero.

<div class="alert"><b>Important</b>  Each member of each structure in this array must be initialized to zero and then set to specific values as necessary. If this is not done, the function will fail in situations that involve remote card readers.</div>
<div> </div>

### -param cReaders [in]

The number of elements in the <i>rgReaderStates</i> array.

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

The <b>SCardGetStatusChange</b> function is a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> tracking function. For more information about other tracking functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-tracking-functions">Smart Card Tracking Functions</a>.


#### Examples

For information about how to call this function, see the  example in 
<a href="/windows/desktop/api/winscard/nf-winscard-scardlocatecardsa">SCardLocateCards</a>.

<div class="code"></div>




> [!NOTE]
> The winscard.h header defines SCardGetStatusChange as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/ns-winscard-scard_readerstatea">SCARD_READERSTATE</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardcancel">SCardCancel</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlocatecardsa">SCardLocateCards</a>
