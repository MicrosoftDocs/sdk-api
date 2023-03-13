---
UID: NN:tapi3.ITAgentSession
title: ITAgentSession (tapi3.h)
description: The methods of ITAgentSession (tapi3.h) allow an application to retrieve statistics. An agent session represents an association between an agent, group, and address.
helpviewer_keywords: ["ITAgentSession","ITAgentSession interface [TAPI 2.2]","ITAgentSession interface [TAPI 2.2]","described","_tapi3_itagentsession","tapi3.itagentsession","tapi3cc/ITAgentSession"]
old-location: tapi3\itagentsession.htm
tech.root: tapi3
ms.assetid: b0db0834-7b9b-4a72-9cc6-6cba31ed1275
ms.date: 08/10/2022
ms.keywords: ITAgentSession, ITAgentSession interface [TAPI 2.2], ITAgentSession interface [TAPI 2.2],described, _tapi3_itagentsession, tapi3.itagentsession, tapi3cc/ITAgentSession
req.header: tapi3.h
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
 - ITAgentSession
 - tapi3/ITAgentSession
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
 - ITAgentSession
---

# ITAgentSession interface


## -description

An agent session represents an association between an agent, group, and address. The methods of 
<b>ITAgentSession</b> allow an application to retrieve a variety of statistics. The following methods create the 
<b>ITAgentSession</b> interface:


<a href="/windows/desktop/api/tapi3/nf-tapi3-ienumagentsession-next">IEnumAgentSession::Next</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-get_agentsessions">ITAgent::get_AgentSessions</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-createsession">ITAgent::CreateSession</a>


See 
<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information.

Note to TAPI 2.1 programmers: Many of the methods in this interface are COM wrappers for 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentsessioninfo">lineGetAgentSessionInfo</a>.

## -inheritance

The <b>ITAgentSession</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAgentSession</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
