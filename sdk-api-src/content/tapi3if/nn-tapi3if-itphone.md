---
UID: NN:tapi3if.ITPhone
title: ITPhone (tapi3if.h)
description: The ITPhone interface is the main interface for the new Phone objects in the TAPI 3.1 object model.
helpviewer_keywords: ["ITPhone","ITPhone interface [TAPI 2.2]","ITPhone interface [TAPI 2.2]","described","_tapi3_itphone","tapi3.itphone","tapi3if/ITPhone"]
old-location: tapi3\itphone.htm
tech.root: tapi3
ms.assetid: 94dff33c-67a1-4df8-9ef5-2b6524438f6f
ms.date: 12/05/2018
ms.keywords: ITPhone, ITPhone interface [TAPI 2.2], ITPhone interface [TAPI 2.2],described, _tapi3_itphone, tapi3.itphone, tapi3if/ITPhone
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
 - ITPhone
 - tapi3if/ITPhone
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
 - ITPhone
---

# ITPhone interface


## -description

The 
<b>ITPhone</b> interface is the main interface for the new Phone objects in the TAPI 3.1 object model. This interface allows access to the phone device at a level comparable to that available with the TAPI 2.<i>x</i> C API. The interface also allows the application to determine which addresses the phone is usable on, and to get a list of terminals associated with the phone. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ienumphone-next">IEnumPhone::Next</a> and <a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_phone">ITPhoneEvent::get_Phone</a> methods create the 
<b>ITPhone</b> interface.

## -inheritance

The <b>ITPhone</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITPhone</b> also has these types of members:

