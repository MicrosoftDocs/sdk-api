---
UID: NN:tapi3cc.ITAgent
title: ITAgent (tapi3cc.h)
description: The ITAgent interface (tapi3cc.h) handles Agent objects, which receive and process incoming calls and make outgoing calls to customers or prospects.
helpviewer_keywords: ["ITAgent","ITAgent interface [TAPI 2.2]","ITAgent interface [TAPI 2.2]","described","_tapi3_itagent","tapi3.itagent","tapi3cc/ITAgent"]
old-location: tapi3\itagent.htm
tech.root: tapi3
ms.assetid: 6c1409c9-da73-4d21-bf56-07e9ab7b33a0
ms.date: 08/10/2022
ms.keywords: ITAgent, ITAgent interface [TAPI 2.2], ITAgent interface [TAPI 2.2],described, _tapi3_itagent, tapi3.itagent, tapi3cc/ITAgent
req.header: tapi3cc.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAgent
 - tapi3cc/ITAgent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgent
---

# ITAgent interface


## -description

Agents are the heart of a call center. They are responsible for receiving and processing incoming calls and, at times, making outgoing calls to customers or prospects. The following methods create the 
<b>ITAgent</b> interface:


<a href="/windows/desktop/api/tapi3/nf-tapi3-ienumagent-next">IEnumAgent::Next</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagentevent-get_agent">ITAgentEvent::get_Agent</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-createagent">ITAgentHandler::CreateAgent</a>


See 
<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information.

## -inheritance

The <b>ITAgent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAgent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
