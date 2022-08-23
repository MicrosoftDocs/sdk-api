---
UID: NN:tapi3cc.ITACDGroup
title: ITACDGroup (tapi3cc.h)
description: The ITACDGroup interface (tapi3cc.h) handles Automatic Call Distribution (ACD) mechanisms, which queue and distribute calls within a switching system.
helpviewer_keywords: ["ITACDGroup","ITACDGroup interface [TAPI 2.2]","ITACDGroup interface [TAPI 2.2]","described","_tapi3_itacdgroup","tapi3.itacdgroup","tapi3cc/ITACDGroup"]
old-location: tapi3\itacdgroup.htm
tech.root: tapi3
ms.assetid: 73e23023-5574-4c5a-bdff-cbc7da765a65
ms.date: 08/10/2022
ms.keywords: ITACDGroup, ITACDGroup interface [TAPI 2.2], ITACDGroup interface [TAPI 2.2],described, _tapi3_itacdgroup, tapi3.itacdgroup, tapi3cc/ITACDGroup
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
 - ITACDGroup
 - tapi3cc/ITACDGroup
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
 - ITACDGroup
---

# ITACDGroup interface


## -description

Automatic Call Distribution (ACD) is a mechanism that queues and distributes calls within a switching system. The ACDGroup object reflects an ACD pilot, split, or group. For example, one ACDGroup might handle calls for new accounts while another handles queries on existing accounts. The following methods create the 
<b>ITACDGroup</b> interface:


<a href="/windows/desktop/api/tapi3/nf-tapi3-ienumacdgroup-next">IEnumACDGroup::Next</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-get_acdgroups">ITAgentHandler::get_ACDGroups</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-createsession">ITAgent::CreateSession</a>


See 
<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information.

## -inheritance

The <b>ITACDGroup</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITACDGroup</b> also has these types of members:

