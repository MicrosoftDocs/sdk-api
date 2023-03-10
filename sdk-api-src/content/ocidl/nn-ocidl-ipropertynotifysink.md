---
UID: NN:ocidl.IPropertyNotifySink
title: IPropertyNotifySink (ocidl.h)
description: Implemented by a sink object to receive notifications about property changes from an object that supports IPropertyNotifySink as an outgoing interface.
helpviewer_keywords: ["IPropertyNotifySink","IPropertyNotifySink interface [COM]","IPropertyNotifySink interface [COM]","described","_ctrl_ipropertynotifysink","com.ipropertynotifysink","ocidl/IPropertyNotifySink"]
old-location: com\ipropertynotifysink.htm
tech.root: com
ms.assetid: bfdf315c-6375-4c77-abd8-03f07342820f
ms.date: 12/05/2018
ms.keywords: IPropertyNotifySink, IPropertyNotifySink interface [COM], IPropertyNotifySink interface [COM],described, _ctrl_ipropertynotifysink, com.ipropertynotifysink, ocidl/IPropertyNotifySink
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IPropertyNotifySink
 - ocidl/IPropertyNotifySink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPropertyNotifySink
---

# IPropertyNotifySink interface


## -description

Implemented by a sink object to receive notifications about property changes from an object that supports <b>IPropertyNotifySink</b> as an outgoing interface. The client that needs to receive the notifications in this interface (from a supporting connectable object) creates a sink with this interface and connects it to the connectable object through the connection point mechanism. For more information on connection points, see <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>.

## -inheritance

The <b>IPropertyNotifySink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyNotifySink</b> also has these types of members:

## -remarks

The object is itself required to call the methods of <b>IPropertyNotifySink</b> only for those properties marked with the [<a href="/windows/desktop/Midl/bindable">bindable</a>] and [<a href="/windows/desktop/Midl/requestedit">requestedit</a>] attributes in the object's type information. When the object changes a [<b>bindable</b>] property, it is required to call <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertynotifysink-onchanged">IPropertyNotifySink::OnChanged</a>. When the object is about to change a [<b>requestedit</b>] property, it must call <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertynotifysink-onrequestedit">IPropertyNotifySink::OnRequestEdit</a> before changing the property and must also honor the action specified by the sink on return from this call.

The one exception to this rule is that no notifications are sent as a result of an object's initialization or loading procedures. At initialization time, it is assumed that all properties change and that all must be allowed to change. Notifications to this interface are therefore meaningful only in the context of a fully initialized/loaded object.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>
