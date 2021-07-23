---
UID: NN:objidl.IPersist
title: IPersist (objidl.h)
description: Provides the CLSID of an object that can be stored persistently in the system. Allows the object to specify which object handler to use in the client process, as it is used in the default implementation of marshaling.
helpviewer_keywords: ["IPersist","IPersist interface [COM]","IPersist interface [COM]","described","_com_ipersist","com.ipersist","objidl/IPersist"]
old-location: com\ipersist.htm
tech.root: com
ms.assetid: 932eb0e2-35a6-482e-9138-00cff30508a9
ms.date: 12/05/2018
ms.keywords: IPersist, IPersist interface [COM], IPersist interface [COM],described, _com_ipersist, com.ipersist, objidl/IPersist
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IPersist
 - objidl/IPersist
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersist
---

# IPersist interface


## -description

Provides the CLSID of an object that can be stored persistently in the system. Allows the object to specify which object handler to use in the client process, as it is used in the default implementation of marshaling.

<b>IPersist</b> is the base interface for three other interfaces: <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>, <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>, and <a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>. Each of these interfaces, therefore, includes the <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">GetClassID</a> method, and the appropriate one of these three interfaces is implemented on objects that can be serialized to a storage, a stream, or a file. The methods of these interfaces allow the state of these objects to be saved for later instantiations, and load the object using the saved state. Typically, the persistence interfaces are implemented by an embedded or linked object, and are called by the container application or the default object handler.

## -inheritance

The <b>IPersist</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPersist</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>
