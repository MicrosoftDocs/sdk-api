---
UID: NN:msp.ITPluggableTerminalEventSink
title: ITPluggableTerminalEventSink (msp.h)
description: The ITPluggableTerminalEventSink interface provides a method that fires a message to notify client applications about a change in a pluggable terminal.helpviewer_keywords: ["ITPluggableTerminalEventSink","ITPluggableTerminalEventSink interface [TAPI 2.2]","ITPluggableTerminalEventSink interface [TAPI 2.2]","described","_tapi3_itpluggableterminaleventsink","msp/ITPluggableTerminalEventSink","tapi3.itpluggableterminaleventsink"]
old-location: tapi3\itpluggableterminaleventsink.htm
tech.root: Tapi
ms.assetid: bcf64c78-aad2-4b53-b938-cc1fd373c8b4
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalEventSink, ITPluggableTerminalEventSink interface [TAPI 2.2], ITPluggableTerminalEventSink interface [TAPI 2.2],described, _tapi3_itpluggableterminaleventsink, msp/ITPluggableTerminalEventSink, tapi3.itpluggableterminaleventsink
f1_keywords:
- msp/ITPluggableTerminalEventSink
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
- ITPluggableTerminalEventSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPluggableTerminalEventSink interface


## -description


The 
<b>ITPluggableTerminalEventSink</b> interface provides a method that fires a message to notify client applications about a change in a pluggable terminal.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPluggableTerminalEventSink</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITPluggableTerminalEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPluggableTerminalEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsink-fireevent">FireEvent</a>
</td>
<td align="left" width="63%">
Notifies the client application of a change in the pluggable terminal.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration">ITPluggableTerminalEventSinkRegistration</a>
 

 

