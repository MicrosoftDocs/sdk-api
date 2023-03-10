---
UID: NF:wct.RegisterWaitChainCOMCallback
title: RegisterWaitChainCOMCallback function (wct.h)
description: Register COM callback functions for WCT.
helpviewer_keywords: ["RegisterWaitChainCOMCallback","RegisterWaitChainCOMCallback function","base.registerwaitchaincomcallback","wct/RegisterWaitChainCOMCallback"]
old-location: base\registerwaitchaincomcallback.htm
tech.root: Debug
ms.assetid: f8adffa3-6e63-4fae-81e8-5f6643e988e9
ms.date: 12/05/2018
ms.keywords: RegisterWaitChainCOMCallback, RegisterWaitChainCOMCallback function, base.registerwaitchaincomcallback, wct/RegisterWaitChainCOMCallback
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
 - RegisterWaitChainCOMCallback
 - wct/RegisterWaitChainCOMCallback
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
 - RegisterWaitChainCOMCallback
---

# RegisterWaitChainCOMCallback function


## -description

Register COM callback functions for WCT.

## -parameters

### -param CallStateCallback [in]

The address of the <b>CoGetCallState</b> function.

### -param ActivationStateCallback [in]

The address of the <b>CoGetActivationState</b> function.

## -remarks

If a thread is blocked on a COM call, WCT can retrieve COM ownership information using these callback functions. If this function is callback multiple times, only the last addresses retrieved are used.


#### Examples

For an example, see 
<a href="/windows/desktop/Debug/using-wct">Using WCT</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Debug/wait-chain-traversal">Wait Chain Traversal</a>