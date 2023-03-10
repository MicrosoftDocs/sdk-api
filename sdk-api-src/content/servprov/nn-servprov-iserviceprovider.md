---
UID: NN:servprov.IServiceProvider
tech.root: com
title: IServiceProvider
ms.date: 08/15/2022
targetos: Windows
description: The IServiceProvider interface provides a generic access mechanism to locate a GUID-identified service.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: servprov.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - servprov.h
api_name:
 - IServiceProvider
f1_keywords:
 - IServiceProvider
 - servprov/IServiceProvider
dev_langs:
 - c++
---

## -description

Provides a generic access mechanism to locate a GUID-identified service.

## -remarks

The **IServiceProvider** interface is a generic access mechanism to locate a GUID-identified service that is provided through a control or any other object that the service can communicate with. For example, an embedded object (such as an OLE control) typically communicates only with its associated client site object in the container through the [IOleClientSite](../oleidl/nn-oleidl-ioleclientsite.md) interface that is supplied by using [IOleObject::SetClientSite](../oleidl/nf-oleidl-ioleobject-setclientsite.md). The embedded object must ask the client site for some other service that the container supports when that service might not be implemented in the client site.

The client site must provide a means by which the control that is managed by the site can access the service when necessary. For example, the [IOleInPlaceSite::GetWindowContext](/windows/win32/api/oleidl/nf-oleidl-ioleinplacesite-getwindowcontext)) function can be used by an in-place object or control to access interface pointers for the document object that contains the site and the frame object that contains the document. Because these interface pointers exist on separate objects, the control cannot call the site's [QueryInterface](../unknwn/nf-unknwn-iunknown-queryinterface(q).md) to obtain those pointers. Instead, use the IServiceProvider interface.

The **IServiceProvider** interface has to overloads of a single method, [QueryService](nf-servprov-iserviceprovider-queryservice(refguid_refiid_void).md), through which a caller specifies the service ID (SID, a GUID), the IID of the interface to return, and the address of the caller's interface pointer variable. The second overload infers the IID from the output pointer passed into the method.

The IID for this interface is IID_IServiceProvider.

## -see-also

