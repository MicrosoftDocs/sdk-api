---
UID: NN:tapi3cc.IEnumACDGroup
title: IEnumACDGroup (tapi3cc.h)
description: The IEnumACDGroup interface (tapi3cc.h) provides COM-standard enumeration methods for the ITACDGroup interface.
helpviewer_keywords: ["IEnumACDGroup","IEnumACDGroup interface [TAPI 2.2]","IEnumACDGroup interface [TAPI 2.2]","described","_tapi3_ienumacdgroup","tapi3.ienumacdgroup","tapi3cc/IEnumACDGroup"]
old-location: tapi3\ienumacdgroup.htm
tech.root: tapi3
ms.assetid: 301cd27e-00ac-44a4-b5c6-0efcb36ad974
ms.date: 08/10/2022
ms.keywords: IEnumACDGroup, IEnumACDGroup interface [TAPI 2.2], IEnumACDGroup interface [TAPI 2.2],described, _tapi3_ienumacdgroup, tapi3.ienumacdgroup, tapi3cc/IEnumACDGroup
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
 - IEnumACDGroup
 - tapi3cc/IEnumACDGroup
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
 - IEnumACDGroup
---

# IEnumACDGroup interface


## -description

The 
<b>IEnumACDGroup</b> interface provides COM-standard enumeration methods for the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a> interface. The 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-enumerateacdgroups">ITAgentHandler::EnumerateACDGroups</a> method returns a pointer to 
<b>IEnumACDGroup</b>.

## -inheritance

The <b>IEnumACDGroup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumACDGroup</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a>
