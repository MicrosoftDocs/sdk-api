---
UID: NN:tapi3.IEnumAgentSession
title: IEnumAgentSession (tapi3.h)
description: The IEnumAgentSession (tapi3.h) interface provides COM-standard enumeration methods for the ITAgentSession interface.
helpviewer_keywords: ["IEnumAgentSession","IEnumAgentSession interface [TAPI 2.2]","IEnumAgentSession interface [TAPI 2.2]","described","_tapi3_ienumagentsession","tapi3.ienumagentsession","tapi3cc/IEnumAgentSession"]
old-location: tapi3\ienumagentsession.htm
tech.root: tapi3
ms.assetid: 38b9fc57-a0af-4dfa-9058-e721138c8be9
ms.date: 08/10/2022
ms.keywords: IEnumAgentSession, IEnumAgentSession interface [TAPI 2.2], IEnumAgentSession interface [TAPI 2.2],described, _tapi3_ienumagentsession, tapi3.ienumagentsession, tapi3cc/IEnumAgentSession
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
 - IEnumAgentSession
 - tapi3/IEnumAgentSession
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
 - IEnumAgentSession
---

# IEnumAgentSession interface


## -description

The 
<b>IEnumAgentSession</b> interface provides COM-standard enumeration methods for the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a> interface. The 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-enumerateagentsessions">ITAgent::EnumerateAgentSessions</a> method returns a pointer to 
<b>IEnumAgentSession</b>.

## -inheritance

The <b>IEnumAgentSession</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumAgentSession</b> also has these types of members:

