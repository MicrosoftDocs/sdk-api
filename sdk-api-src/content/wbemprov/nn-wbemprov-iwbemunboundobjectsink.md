---
UID: NN:wbemprov.IWbemUnboundObjectSink
title: IWbemUnboundObjectSink
author: windows-sdk-content
description: The IWbemUnboundObjectSink interface is implemented by all logical event consumers. It is a simple sink interface that accepts delivery of event objects.
old-location: wmi\iwbemunboundobjectsink.htm
tech.root: WmiSdk
ms.assetid: a890aefe-e35e-4635-874d-953194f99a82
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWbemUnboundObjectSink, IWbemUnboundObjectSink interface [Windows Management Instrumentation], IWbemUnboundObjectSink interface [Windows Management Instrumentation],described, _hmm_iwbemunboundobjectsink, wbemprov/IWbemUnboundObjectSink, wmi.iwbemunboundobjectsink
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
api_name:
 - IWbemUnboundObjectSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemUnboundObjectSink interface


## -description


The 
<b>IWbemUnboundObjectSink</b> interface is implemented by all logical event consumers. It is a simple sink interface that accepts delivery of event objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemUnboundObjectSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemUnboundObjectSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemUnboundObjectSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70fe9976-cfa9-442d-93a4-12293e80d1fa">IndicateToConsumer</a>
</td>
<td align="left" width="63%">
Called by Windows Management to actually deliver events to a consumer.

</td>
</tr>
</table> 

