---
UID: NN:oaidl.ITypeChangeEvents
title: ITypeChangeEvents (oaidl.h)
description: Enables clients to subscribe to type change notifications on objects that implement the ITypeInfo, ITypeInfo2, ICreateTypeInfo, and ICreateTypeInfo2 interfaces.
helpviewer_keywords: ["ITypeChangeEvents","ITypeChangeEvents interface [Automation]","ITypeChangeEvents interface [Automation]","described","automat.itypechangeevents","oaidl/ITypeChangeEvents"]
old-location: automat\itypechangeevents.htm
tech.root: automat
ms.assetid: 5e286a4b-b36b-40d6-9a39-d572086e5a2d
ms.date: 12/05/2018
ms.keywords: ITypeChangeEvents, ITypeChangeEvents interface [Automation], ITypeChangeEvents interface [Automation],described, automat.itypechangeevents, oaidl/ITypeChangeEvents
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITypeChangeEvents
 - oaidl/ITypeChangeEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ITypeChangeEvents
---

# ITypeChangeEvents interface


## -description

Enables clients to subscribe to type change notifications on objects that implement the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a>, <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo2">ITypeInfo2</a>, <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo">ICreateTypeInfo</a>, and <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreatetypeinfo2">ICreateTypeInfo2</a> interfaces. When ITypeChangeEvents is implemented on an object, it acts as an incoming interface that enables the object to receive calls from external clients and engage in bidirectional communication with those clients. For more information, see <a href="/windows/desktop/com/events-in-com-and-connectable-objects">Events in COM and Connectable Objects</a>.

## -inheritance

The <b>ITypeChangeEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITypeChangeEvents</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/automat/using-type-building-interfaces-and-functions">Type Building Interfaces and Functions </a>
