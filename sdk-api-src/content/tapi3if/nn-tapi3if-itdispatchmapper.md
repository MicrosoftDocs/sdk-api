---
UID: NN:tapi3if.ITDispatchMapper
title: ITDispatchMapper (tapi3if.h)
description: The ITDispatchMapper interface allows an application to retrieve the dispatch pointer of another interface on an object, given the dispatch pointer of one interface and the GUID of another.
helpviewer_keywords: ["ITDispatchMapper","ITDispatchMapper interface [TAPI 2.2]","ITDispatchMapper interface [TAPI 2.2]","described","_tapi3_itdispatchmapper","tapi3.itdispatchmapper","tapi3if/ITDispatchMapper"]
old-location: tapi3\itdispatchmapper.htm
tech.root: tapi3
ms.assetid: 65286ea6-b9a6-423b-9833-2d41ef2fd8de
ms.date: 12/05/2018
ms.keywords: ITDispatchMapper, ITDispatchMapper interface [TAPI 2.2], ITDispatchMapper interface [TAPI 2.2],described, _tapi3_itdispatchmapper, tapi3.itdispatchmapper, tapi3if/ITDispatchMapper
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
 - ITDispatchMapper
 - tapi3if/ITDispatchMapper
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
 - ITDispatchMapper
---

# ITDispatchMapper interface


## -description

The 
<b>ITDispatchMapper</b> interface allows an application to retrieve the dispatch pointer of another interface on an object, given the dispatch pointer of one interface and the GUID of another. This interface is provided to assist programmers using scripting applications which do not automatically support tracking of multiple interfaces on an object.

The Dispatch Mapper will use the object's <b>IObjectSafety</b> interface to make sure the object is safe for scripting on the requested interface. If the object does not implement <b>IObjectSafety</b>, or if the object is not safe on this particular interface, the call will fail.

The 
<a href="/windows/desktop/Tapi/dispatch-mapper">Dispatch Mapper</a> object must be created using COM <b>CoCreateInstance</b>.

## -inheritance

The <b>ITDispatchMapper</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITDispatchMapper</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/dispatch-mapper">Dispatch Mapper</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
