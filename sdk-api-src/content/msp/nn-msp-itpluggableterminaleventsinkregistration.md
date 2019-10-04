---
UID: NN:msp.ITPluggableTerminalEventSinkRegistration
title: ITPluggableTerminalEventSinkRegistration (msp.h)
author: windows-sdk-content
description: The ITPluggableTerminalEventSinkRegistration interface registers and unregisters a client application for pluggable terminal events. The ITPluggableTerminalEventSinkRegistration interface is created by calling QueryInterface on ITTerminal.
old-location: tapi3\itpluggableterminaleventsinkregistration.htm
tech.root: Tapi
ms.assetid: 4c8924bd-468e-458c-b16a-ac378fb4b69a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalEventSinkRegistration, ITPluggableTerminalEventSinkRegistration interface [TAPI 2.2], ITPluggableTerminalEventSinkRegistration interface [TAPI 2.2],described, _tapi3_itpluggableterminaleventsinkregistration, msp/ITPluggableTerminalEventSinkRegistration, tapi3.itpluggableterminaleventsinkregistration
ms.topic: interface
f1_keywords: 
 - "msp/ITPluggableTerminalEventSinkRegistration"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalEventSinkRegistration interface


## -description


The 
<b>ITPluggableTerminalEventSinkRegistration</b> interface registers and unregisters a client application for pluggable terminal events. The 
<b>ITPluggableTerminalEventSinkRegistration</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalEventSinkRegistration</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITPluggableTerminalEventSinkRegistration</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink">RegisterSink</a>
</td>
<td align="left" width="63%">
Register for pluggable terminal events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink">UnregisterSink</a>
</td>
<td align="left" width="63%">
Unregister for pluggable terminal events.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink">ITPluggableTerminalEventSink</a>
 

 

