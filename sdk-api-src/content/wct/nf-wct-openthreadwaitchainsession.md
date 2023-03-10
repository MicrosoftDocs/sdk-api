---
UID: NF:wct.OpenThreadWaitChainSession
title: OpenThreadWaitChainSession function (wct.h)
description: Creates a new WCT session.
helpviewer_keywords: ["OpenThreadWaitChainSession","OpenThreadWaitChainSession function","WCT_ASYNC_OPEN_FLAG","base.openthreadwaitchainsession","wct/OpenThreadWaitChainSession"]
old-location: base\openthreadwaitchainsession.htm
tech.root: Debug
ms.assetid: 405d9f3d-c11b-4e20-acc8-9c4f7989685d
ms.date: 12/05/2018
ms.keywords: OpenThreadWaitChainSession, OpenThreadWaitChainSession function, WCT_ASYNC_OPEN_FLAG, base.openthreadwaitchainsession, wct/OpenThreadWaitChainSession
req.header: wct.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OpenThreadWaitChainSession
 - wct/OpenThreadWaitChainSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-MS-Win-wer-wct-l1-1-0.dll
 - wer.dll
api_name:
 - OpenThreadWaitChainSession
---

# OpenThreadWaitChainSession function


## -description

Creates a new WCT session.

## -parameters

### -param Flags [in]

The session type. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
A synchronous session.

</td>
</tr>
<tr>
<td width="40%"><a id="WCT_ASYNC_OPEN_FLAG"></a><a id="wct_async_open_flag"></a><dl>
<dt><b>WCT_ASYNC_OPEN_FLAG</b></dt>
</dl>
</td>
<td width="60%">
An asynchronous session.

</td>
</tr>
</table>

### -param callback [in, optional]

If the session is asynchronous, this parameter can be a pointer to a <a href="/windows/desktop/api/wct/nc-wct-pwaitchaincallback">WaitChainCallback</a> callback function.

## -returns

If the function succeeds, the return value is a handle to the newly created session.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When you have finished using the session, call the <a href="/windows/desktop/api/wct/nf-wct-closethreadwaitchainsession">CloseThreadWaitChainSession</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/Debug/using-wct">Using WCT</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wct/nf-wct-closethreadwaitchainsession">CloseThreadWaitChainSession</a>



<a href="/windows/desktop/api/wct/nf-wct-getthreadwaitchain">GetThreadWaitChain</a>



<a href="/windows/desktop/Debug/wait-chain-traversal">Wait Chain Traversal</a>



<a href="/windows/desktop/api/wct/nc-wct-pwaitchaincallback">WaitChainCallback</a>