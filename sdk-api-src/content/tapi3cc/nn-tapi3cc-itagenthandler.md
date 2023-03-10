---
UID: NN:tapi3cc.ITAgentHandler
title: ITAgentHandler (tapi3cc.h)
description: The ITAgentHandler interface (tapi3cc.h) provides methods to create Agent objects and enumerate Automatic Call Distribution (ACD) groups.
helpviewer_keywords: ["ITAgentHandler","ITAgentHandler interface [TAPI 2.2]","ITAgentHandler interface [TAPI 2.2]","described","_tapi3_itagenthandler","tapi3.itagenthandler","tapi3cc/ITAgentHandler"]
old-location: tapi3\itagenthandler.htm
tech.root: tapi3
ms.assetid: 11861d77-39ad-4d85-bf68-ba0f4321ba7c
ms.date: 08/10/2022
ms.keywords: ITAgentHandler, ITAgentHandler interface [TAPI 2.2], ITAgentHandler interface [TAPI 2.2],described, _tapi3_itagenthandler, tapi3.itagenthandler, tapi3cc/ITAgentHandler
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
 - ITAgentHandler
 - tapi3cc/ITAgentHandler
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
 - ITAgentHandler
---

# ITAgentHandler interface


## -description

The 
<b>ITAgentHandler</b> interface provides methods to create Agent objects and enumerate Automatic Call Distribution (ACD) groups. The 
<a href="/windows/desktop/api/tapi3/nf-tapi3-ienumagenthandler-next">IEnumAgentHandler::Next</a> and 
<a href="/windows/desktop/api/tapi3/nf-tapi3-ittapicallcenter-get_agenthandlers">ITTapiCallCenter::get_AgentHandlers</a> methods create the 
<b>ITAgentHandler</b> interface.

## -inheritance

The <b>ITAgentHandler</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAgentHandler</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>
