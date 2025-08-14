---
UID: NF:winscard.SCardCancel
title: SCardCancel function (winscard.h)
description: Terminates all outstanding actions within a specific resource manager context.
helpviewer_keywords: ["SCardCancel","SCardCancel function [Security]","_smart_scardcancel","security.scardcancel","winscard/SCardCancel"]
old-location: security\scardcancel.htm
tech.root: security
ms.assetid: abf3b4ff-4775-40e9-b68d-97dcf6a892ba
ms.date: 12/05/2018
ms.keywords: SCardCancel, SCardCancel function [Security], _smart_scardcancel, security.scardcancel, winscard/SCardCancel
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
 - SCardCancel
 - winscard/SCardCancel
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
 - SCardCancel
---

# SCardCancel function


## -description

The <b>SCardCancel</b> function terminates all outstanding actions within a specific <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>.

The only requests that you can cancel are those that require waiting for external action by the <a href="/windows/desktop/SecGloss/s-gly">smart card</a> or user. Any such outstanding action requests will terminate with a status indication that the action was canceled. This is especially useful to force outstanding <a href="/windows/desktop/api/winscard/nf-winscard-scardgetstatuschangea">SCardGetStatusChange</a> calls to terminate.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>.

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

The <b>SCardCancel</b> function is a smart card tracking function. For a description of other tracking functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-tracking-functions">Smart Card Tracking Functions</a>.


#### Examples

The following example cancels all outstanding actions in the specified context.  The example assumes that lReturn is an existing variable of type <b>LONG</b> and that hContext is a valid handle received from a previous call to <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. 


```cpp

lReturn = SCardCancel( hContext );
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardCancel\n");

```

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardgetstatuschangea">SCardGetStatusChange</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlocatecardsa">SCardLocateCards</a>