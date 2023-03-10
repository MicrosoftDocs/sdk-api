---
UID: NN:tapi3if.ITTAPI
title: ITTAPI (tapi3if.h)
description: The ITTAPI interface is the base interface for the TAPI object. The TAPI object is created by CoCreateInstance. For information on CoCreateInstance, see documentation on COM. All other TAPI 3 objects are created by TAPI 3 itself.
helpviewer_keywords: ["ITTAPI","ITTAPI interface [TAPI 2.2]","ITTAPI interface [TAPI 2.2]","described","_tapi3_ittapi","tapi3.ittapi","tapi3if/ITTAPI"]
old-location: tapi3\ittapi.htm
tech.root: tapi3
ms.assetid: 75d641c7-dbf8-4ae2-b16b-2757e890d32b
ms.date: 12/05/2018
ms.keywords: ITTAPI, ITTAPI interface [TAPI 2.2], ITTAPI interface [TAPI 2.2],described, _tapi3_ittapi, tapi3.ittapi, tapi3if/ITTAPI
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
 - ITTAPI
 - tapi3if/ITTAPI
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
 - ITTAPI
---

# ITTAPI interface


## -description

The 
<b>ITTAPI</b> interface is the base interface for the TAPI object. The TAPI object is created by <b>CoCreateInstance</b>. For information on <b>CoCreateInstance</b>, see documentation on COM. All other TAPI 3 objects are created by TAPI 3 itself.

<b>ITTAPI</b> methods are provided to initialize a TAPI session, enumerate available addresses, register for CallHub and CallEvent notifications, and shut down a TAPI session.

The 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2">ITTAPI2</a> interface derives from the 
<b>ITTAPI</b> interface. It adds additional methods on the TAPI object to support phone devices.

## -inheritance

The <b>ITTAPI</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTAPI</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2">ITTAPI2</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>
