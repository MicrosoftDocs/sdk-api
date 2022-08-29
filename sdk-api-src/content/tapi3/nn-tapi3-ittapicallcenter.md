---
UID: NN:tapi3.ITTAPICallCenter
title: ITTAPICallCenter (tapi3.h)
description: The ITTAPICallCenter interface (tapi3.h) provides an entry point into call center controls. 
helpviewer_keywords: ["ITTAPICallCenter","ITTAPICallCenter interface [TAPI 2.2]","ITTAPICallCenter interface [TAPI 2.2]","described","_tapi3_ittapicallcenter","tapi3.ittapicallcenter","tapi3cc/ITTAPICallCenter"]
old-location: tapi3\ittapicallcenter.htm
tech.root: tapi3
ms.assetid: 871cb217-a44f-421e-9cb4-7d8771335d08
ms.date: 08/09/2022
ms.keywords: ITTAPICallCenter, ITTAPICallCenter interface [TAPI 2.2], ITTAPICallCenter interface [TAPI 2.2],described, _tapi3_ittapicallcenter, tapi3.ittapicallcenter, tapi3cc/ITTAPICallCenter
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
 - ITTAPICallCenter
 - tapi3/ITTAPICallCenter
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
 - ITTAPICallCenter
---

# ITTAPICallCenter interface


## -description

The 
<b>ITTAPICallCenter</b> interface provides an entry point into call center controls. It exposes methods that allow an application to discover available agent handlers. The agent handler interface can then be used to access the other elements of a call center, such as ACD groups, agents, and queues.

The 
<b>ITTAPICallCenter</b> interface is created by calling <b>QueryInterface</b> on 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>.

Please see 
<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information.

## -inheritance

The <b>ITTAPICallCenter</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTAPICallCenter</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/call-center-controls-interfaces">Call Center Interfaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>
