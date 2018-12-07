---
UID: NF:wct.RegisterWaitChainCOMCallback
title: RegisterWaitChainCOMCallback function
author: windows-sdk-content
description: Register COM callback functions for WCT.
old-location: base\registerwaitchaincomcallback.htm
tech.root: debug
ms.assetid: f8adffa3-6e63-4fae-81e8-5f6643e988e9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RegisterWaitChainCOMCallback, RegisterWaitChainCOMCallback function, base.registerwaitchaincomcallback, wct/RegisterWaitChainCOMCallback
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
 - RegisterWaitChainCOMCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegisterWaitChainCOMCallback function


## -description


Register COM callback functions for WCT.


## -parameters




### -param CallStateCallback [in]

The address of the <b>CoGetCallState</b> function.


### -param ActivationStateCallback [in]

The address of the <b>CoGetActivationState</b> function.


## -returns



This function does not return a value.




## -remarks



If a thread is blocked on a COM call, WCT can retrieve COM ownership information using these callback functions. If this function is callback multiple times, only the last addresses retrieved are used.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/7c5fa606-6e9b-41da-bfa9-1f066449d813">Using WCT</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d266a663-b101-4936-9574-f6ce223419ae">Wait Chain Traversal</a>
 

 

