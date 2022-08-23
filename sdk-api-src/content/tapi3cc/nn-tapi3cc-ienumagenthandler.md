---
UID: NN:tapi3cc.IEnumAgentHandler
title: IEnumAgentHandler (tapi3cc.h)
description: The IEnumAgentHandler interface (tapi3cc.h) provides COM-standard enumeration methods for the ITAgentHandler interface.
helpviewer_keywords: ["IEnumAgentHandler","IEnumAgentHandler interface [TAPI 2.2]","IEnumAgentHandler interface [TAPI 2.2]","described","_tapi3_ienumagenthandler","tapi3.ienumagenthandler","tapi3cc/IEnumAgentHandler"]
old-location: tapi3\ienumagenthandler.htm
tech.root: tapi3
ms.assetid: a318318a-769e-4619-a461-4988d90d3f1a
ms.date: 08/10/2022
ms.keywords: IEnumAgentHandler, IEnumAgentHandler interface [TAPI 2.2], IEnumAgentHandler interface [TAPI 2.2],described, _tapi3_ienumagenthandler, tapi3.ienumagenthandler, tapi3cc/IEnumAgentHandler
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
 - IEnumAgentHandler
 - tapi3cc/IEnumAgentHandler
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
 - IEnumAgentHandler
---

# IEnumAgentHandler interface


## -description

The 
<b>IEnumAgentHandler</b> interface provides COM-standard enumeration methods for the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a> interface. The 
<a href="/windows/desktop/api/tapi3/nf-tapi3-ittapicallcenter-enumerateagenthandlers">ITTAPICallCenter::EnumerateAgentHandlers</a> method returns a pointer to 
<b>IEnumAgentHandler</b>.

## -inheritance

The <b>IEnumAgentHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumAgentHandler</b> also has these types of members:

