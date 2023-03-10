---
UID: NF:wct.CloseThreadWaitChainSession
title: CloseThreadWaitChainSession function (wct.h)
description: Closes the specified WCT session and cancels any outstanding asynchronous operations.
helpviewer_keywords: ["CloseThreadWaitChainSession","CloseThreadWaitChainSession function","base.closethreadwaitchainsession","wct/CloseThreadWaitChainSession"]
old-location: base\closethreadwaitchainsession.htm
tech.root: Debug
ms.assetid: dc288418-01e4-4737-9c63-e6e6b73b5d13
ms.date: 12/05/2018
ms.keywords: CloseThreadWaitChainSession, CloseThreadWaitChainSession function, base.closethreadwaitchainsession, wct/CloseThreadWaitChainSession
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
 - CloseThreadWaitChainSession
 - wct/CloseThreadWaitChainSession
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
 - CloseThreadWaitChainSession
---

# CloseThreadWaitChainSession function


## -description

Closes the specified WCT session and cancels any outstanding asynchronous operations.

## -parameters

### -param WctHandle [in]

A handle to the WCT session created by the <a href="/windows/desktop/api/wct/nf-wct-openthreadwaitchainsession">OpenThreadWaitChainSession</a> function.

## -remarks

If the WCT session was opened in asynchronous mode (with WCT_ASYNC_OPEN_FLAG), the function cancels any outstanding operations after their callback functions have been called and returned, and then it returns.


#### Examples

For an example, see 
<a href="/windows/desktop/Debug/using-wct">Using WCT</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wct/nf-wct-openthreadwaitchainsession">OpenThreadWaitChainSession</a>



<a href="/windows/desktop/Debug/wait-chain-traversal">Wait Chain Traversal</a>