---
UID: NN:wbemprov.IWbemProviderInitSink
title: IWbemProviderInitSink
author: windows-sdk-content
description: The IWbemProviderInitSink interface is implemented by WMI and called by providers to report initialization status.
old-location: wmi\iwbemproviderinitsink.htm
old-project: WmiSdk
ms.assetid: abcee170-6a28-44d2-97d6-cb62c393b534
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IWbemProviderInitSink, IWbemProviderInitSink interface [Windows Management Instrumentation], IWbemProviderInitSink interface [Windows Management Instrumentation],described, _hmm_iwbemproviderinitsink, wbemprov/IWbemProviderInitSink, wmi.iwbemproviderinitsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemprov.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemProviderInitSink
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemProviderInitSink interface


## -description


The 
<b>IWbemProviderInitSink</b> interface is implemented by WMI and called by providers to report initialization status.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemProviderInitSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemProviderInitSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemProviderInitSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/909935ba-ae3a-477d-a466-1f2679764b10">SetStatus</a>
</td>
<td align="left" width="63%">
Called by the provider to indicate success or failure of initialization.

</td>
</tr>
</table> 

