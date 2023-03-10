---
UID: NS:objidl.tagMULTI_QI
title: MULTI_QI (objidl.h)
description: The MULTI_QI (objidl.h) structure represents an interface in a query for multiple interfaces.
helpviewer_keywords: ["MULTI_QI","MULTI_QI structure [COM]","_com_MULTI_QI","com.multi_qi","objidlbase/MULTI_QI","tagMULTI_QI"]
old-location: com\multi_qi.htm
tech.root: com
ms.assetid: 845040c9-fad4-4ac8-856d-d35edbf48ec9
ms.date: 08/13/2022
ms.keywords: MULTI_QI, MULTI_QI structure [COM], _com_MULTI_QI, com.multi_qi, objidlbase/MULTI_QI, tagMULTI_QI
req.header: objidl.h
req.include-header: Objidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MULTI_QI
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMULTI_QI
 - objidl/tagMULTI_QI
 - MULTI_QI
 - objidl/MULTI_QI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - MULTI_QI
---

# MULTI_QI structure


## -description

Represents an interface in a query for multiple interfaces.

## -struct-fields

### -field pIID

A pointer to an interface identifier.

### -field pItf

A pointer to the interface requested in <b>pIID</b>. This member must be <b>NULL</b> on input.

### -field hr

The return value of the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> call to locate the requested interface. Common return values include S_OK and E_NOINTERFACE. This member must be 0 on input.

## -remarks

To optimize network performance, most remote activation functions take an array of <b>MULTI_QI</b> structures rather than just a single IID as input and a single pointer to the requested interface on the object as output, as do local activation functions. This allows a set of pointers to interfaces to be returned from the same object in a single round-trip to the server. In network scenarios, requesting multiple interfaces at the time of object construction can save considerable time over using a number of calls to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for unique interfaces, each of which would require a round-trip to the server.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a>



<a href="/windows/desktop/api/objbase/nf-objbase-cogetinstancefromfile">CoGetInstanceFromFile</a>



<a href="/windows/desktop/api/objbase/nf-objbase-cogetinstancefromistorage">CoGetInstanceFromIStorage</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imultiqi">IMultiQI</a>
