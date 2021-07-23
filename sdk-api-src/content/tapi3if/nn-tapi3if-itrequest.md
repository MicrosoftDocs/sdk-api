---
UID: NN:tapi3if.ITRequest
title: ITRequest (tapi3if.h)
description: The ITRequest interface allows an application to use Assisted Telephony. Assisted Telephony provides telephony-enabled applications with a simple mechanism for making phone calls without requiring the developer to become fully literate in telephony.
helpviewer_keywords: ["ITRequest","ITRequest interface [TAPI 2.2]","ITRequest interface [TAPI 2.2]","described","_tapi3_itrequest","tapi3.itrequest","tapi3if/ITRequest"]
old-location: tapi3\itrequest.htm
tech.root: tapi3
ms.assetid: 2b6d4f99-3ffe-44ce-9cb5-3fdd565085db
ms.date: 12/05/2018
ms.keywords: ITRequest, ITRequest interface [TAPI 2.2], ITRequest interface [TAPI 2.2],described, _tapi3_itrequest, tapi3.itrequest, tapi3if/ITRequest
req.header: tapi3if.h
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
 - ITRequest
 - tapi3if/ITRequest
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
 - ITRequest
---

# ITRequest interface


## -description

The 
<b>ITRequest</b> interface allows an application to use 
<a href="/windows/desktop/Tapi/assisted-telephony-overview">Assisted Telephony</a>. Assisted Telephony provides telephony-enabled applications with a simple mechanism for making phone calls without requiring the developer to become fully literate in telephony.

The Request object must be created using COM <b>CoCreateInstance</b>.

## -inheritance

The <b>ITRequest</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITRequest</b> also has these types of members:

