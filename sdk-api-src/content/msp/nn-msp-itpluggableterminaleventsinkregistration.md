---
UID: NN:msp.ITPluggableTerminalEventSinkRegistration
title: ITPluggableTerminalEventSinkRegistration
author: windows-sdk-content
description: The ITPluggableTerminalEventSinkRegistration interface registers and unregisters a client application for pluggable terminal events. The ITPluggableTerminalEventSinkRegistration interface is created by calling QueryInterface on ITTerminal.
old-location: tapi3\itpluggableterminaleventsinkregistration.htm
tech.root: Tapi
ms.assetid: 4c8924bd-468e-458c-b16a-ac378fb4b69a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITPluggableTerminalEventSinkRegistration, ITPluggableTerminalEventSinkRegistration interface [TAPI 2.2], ITPluggableTerminalEventSinkRegistration interface [TAPI 2.2],described, _tapi3_itpluggableterminaleventsinkregistration, msp/ITPluggableTerminalEventSinkRegistration, tapi3.itpluggableterminaleventsinkregistration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msp.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalEventSinkRegistration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalEventSinkRegistration interface


## -description


The 
<b>ITPluggableTerminalEventSinkRegistration</b> interface registers and unregisters a client application for pluggable terminal events. The 
<b>ITPluggableTerminalEventSinkRegistration</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalEventSinkRegistration</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITPluggableTerminalEventSinkRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPluggableTerminalEventSinkRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4887d299-8c63-4ead-b456-e80417e6ec56">RegisterSink</a>
</td>
<td align="left" width="63%">
Register for pluggable terminal events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/261ea39e-485f-4039-94b0-cd92f614c0a9">UnregisterSink</a>
</td>
<td align="left" width="63%">
Unregister for pluggable terminal events.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bcf64c78-aad2-4b53-b938-cc1fd373c8b4">ITPluggableTerminalEventSink</a>
 

 

