---
UID: NF:winscard.SCardFreeMemory
title: SCardFreeMemory function (winscard.h)
description: Releases memory that has been returned from the resource manager using the SCARD_AUTOALLOCATE length designator.
helpviewer_keywords: ["SCardFreeMemory","SCardFreeMemory function [Security]","_smart_scardfreememory","security.scardfreememory","winscard/SCardFreeMemory"]
old-location: security\scardfreememory.htm
tech.root: security
ms.assetid: d41d3891-671b-4129-8034-b251af983830
ms.date: 12/05/2018
ms.keywords: SCardFreeMemory, SCardFreeMemory function [Security], _smart_scardfreememory, security.scardfreememory, winscard/SCardFreeMemory
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
 - SCardFreeMemory
 - winscard/SCardFreeMemory
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
 - SCardFreeMemory
---

# SCardFreeMemory function


## -description

The <b>SCardFreeMemory</b> function releases memory that has been returned from the <a href="/windows/desktop/SecGloss/r-gly">resource manager</a> using the SCARD_AUTOALLOCATE length designator.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a> returned from <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>, or <b>NULL</b> if the creating function also specified <b>NULL</b> for its <i>hContext</i> parameter. For more information, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-query-functions">Smart Card Database Query Functions</a>.

### -param pvMem [in]

Memory block to be released.

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



<a href="/windows/desktop/api/winscard/nf-winscard-scardgetproviderida">SCardGetProviderId</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistcardsa">SCardListCards</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistinterfacesa">SCardListInterfaces</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistreadergroupsa">SCardListReaderGroups</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistreadersa">SCardListReaders</a>