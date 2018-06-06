---
UID: NN:wbemprov.IWbemEventProviderQuerySink
title: IWbemEventProviderQuerySink
author: windows-sdk-content
description: The IWbemEventProviderQuerySink interface is optionally implemented by event providers who want to know what kinds of event query filters are currently active to optimize performance.
old-location: wmi\iwbemeventproviderquerysink.htm
old-project: WmiSdk
ms.assetid: 76a29d81-33c2-489f-a71d-2e85ba2617bf
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IWbemEventProviderQuerySink, IWbemEventProviderQuerySink interface [Windows Management Instrumentation], IWbemEventProviderQuerySink interface [Windows Management Instrumentation],described, _hmm_iwbemeventproviderquerysink, wbemprov/IWbemEventProviderQuerySink, wmi.iwbemeventproviderquerysink
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
 - IWbemEventProviderQuerySink
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemEventProviderQuerySink interface


## -description


The 
<b>IWbemEventProviderQuerySink</b> interface is optionally implemented by event providers who want to know what kinds of event query filters are currently active to optimize performance.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemEventProviderQuerySink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemEventProviderQuerySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemEventProviderQuerySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fdb56ea9-bd1a-436e-aaa7-3ae11e10f38e">CancelQuery</a>
</td>
<td align="left" width="63%">
Called whenever a consumer query is canceled or unregistered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82f76b19-2035-4567-b619-31ce8a35e422">NewQuery</a>
</td>
<td align="left" width="63%">
Called whenever a new consumer query is registered with WMI.

</td>
</tr>
</table> 


## -remarks



Although WMI calls the methods of 
<a href="https://msdn.microsoft.com/4b92923a-659d-4340-8843-eb42aea69d47">IWbemEventProvider</a> only one time after an event provider becomes active, WMI calls the methods of 
<b>IWbemEventProviderQuerySink</b> continuously, as appropriate. The provider can ignore all calls to 
<b>IWbemEventProviderQuerySink</b> methods as needed. This point is very important; supporting 
<b>IWbemEventProviderQuerySink</b> indicates that a provider will supply at least the events requested by queries.

A provider can also generate more events than requested, which WMI filters as appropriate. This functionality means you can implement 
<b>IWbemEventProviderQuerySink</b> and optimize processing without addressing all parts of the WMI Query Language (WQL). For instance, if a provider does not specifically handle a particular query, the provider can generate all possible events for the query.



