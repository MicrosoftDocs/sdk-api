---
UID: NF:wct.CloseThreadWaitChainSession
title: CloseThreadWaitChainSession function
author: windows-sdk-content
description: Closes the specified WCT session and cancels any outstanding asynchronous operations.
old-location: base\closethreadwaitchainsession.htm
tech.root: debug
ms.assetid: dc288418-01e4-4737-9c63-e6e6b73b5d13
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: CloseThreadWaitChainSession, CloseThreadWaitChainSession function, base.closethreadwaitchainsession, wct/CloseThreadWaitChainSession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CloseThreadWaitChainSession
: 
---

# CloseThreadWaitChainSession function


## -description


Closes the specified WCT session and cancels any outstanding asynchronous operations.


## -parameters




### -param WctHandle [in]

A handle to the WCT session created by the <a href="https://msdn.microsoft.com/405d9f3d-c11b-4e20-acc8-9c4f7989685d">OpenThreadWaitChainSession</a> function.


## -returns



This function does not return a value.




## -remarks



If the WCT session was opened in asynchronous mode (with WCT_ASYNC_OPEN_FLAG), the function cancels any outstanding operations after their callback functions have been called and returned, and then it returns.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/7c5fa606-6e9b-41da-bfa9-1f066449d813">Using WCT</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/405d9f3d-c11b-4e20-acc8-9c4f7989685d">OpenThreadWaitChainSession</a>



<a href="https://msdn.microsoft.com/d266a663-b101-4936-9574-f6ce223419ae">Wait Chain Traversal</a>
 

 

