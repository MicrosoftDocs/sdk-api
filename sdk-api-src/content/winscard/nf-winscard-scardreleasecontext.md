---
UID: NF:winscard.SCardReleaseContext
title: SCardReleaseContext function (winscard.h)
description: Closes an established resource manager context, freeing any resources allocated under that context, including SCARDHANDLE objects and memory allocated using the SCARD_AUTOALLOCATE length designator.
helpviewer_keywords: ["SCardReleaseContext","SCardReleaseContext function [Security]","_smart_scardreleasecontext","security.scardreleasecontext","winscard/SCardReleaseContext"]
old-location: security\scardreleasecontext.htm
tech.root: security
ms.assetid: aa17cf94-ca66-4b5e-b1cd-00319f496b09
ms.date: 12/05/2018
ms.keywords: SCardReleaseContext, SCardReleaseContext function [Security], _smart_scardreleasecontext, security.scardreleasecontext, winscard/SCardReleaseContext
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
 - SCardReleaseContext
 - winscard/SCardReleaseContext
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
 - SCardReleaseContext
---

# SCardReleaseContext function


## -description

The <b>SCardReleaseContext</b> function closes an established <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>, freeing any resources allocated under that context, including SCARDHANDLE objects and memory allocated using the SCARD_AUTOALLOCATE length designator.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>.

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

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>