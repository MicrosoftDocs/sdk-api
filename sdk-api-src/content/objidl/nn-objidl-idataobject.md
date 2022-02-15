---
UID: NN:objidl.IDataObject
title: IDataObject (objidl.h)
description: Enables data transfer and notification of changes in data.
helpviewer_keywords: ["IDataObject","IDataObject interface [COM]","IDataObject interface [COM]","described","_ole_idataobject","com.idataobject","objidl/IDataObject"]
old-location: com\idataobject.htm
tech.root: com
ms.assetid: 8a002deb-2727-456c-8078-a9b0d5893ed4
ms.date: 12/05/2018
ms.keywords: IDataObject, IDataObject interface [COM], IDataObject interface [COM],described, _ole_idataobject, com.idataobject, objidl/IDataObject
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - IDataObject
 - objidl/IDataObject
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
 - IDataObject
---

# IDataObject interface


## -description

Enables data transfer and notification of changes in data. Data transfer methods specify the format of the transferred data along with the medium through which the data is to be transferred. Optionally, the data can be rendered for a specific target device. In addition to methods for retrieving and storing data, the <b>IDataObject</b> interface specifies methods for enumerating available formats and managing connections to advisory sinks for handling change notifications.

The term <i>data object</i> is used to mean any object that supports an implementation of the <b>IDataObject</b> interface. Implementations vary, depending on what the data object is required to do; in some data objects, the implementation of certain methods not supported by the object could simply be the return of E_NOTIMPL. For example, some data objects do not allow callers to send them data. Other data objects do not support advisory connections and change notifications. However, for those data objects that do support change notifications, OLE provides an object called a data advise holder. An interface pointer to this holder is available through a call to the helper function <a href="/windows/desktop/api/ole2/nf-ole2-createdataadviseholder">CreateDataAdviseHolder</a>. A data object can have multiple connections, each with its own set of attributes. The OLE data advise holder simplifies the task of managing these connections and sending the appropriate notifications.

## -inheritance

The <b>IDataObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDataObject</b> also has these types of members:

