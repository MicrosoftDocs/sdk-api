---
UID: NN:objidl.IPersistStorage
title: IPersistStorage (objidl.h)
description: Enables a container application to pass a storage object to one of its contained objects and to load and save the storage object.
helpviewer_keywords: ["IPersistStorage","IPersistStorage interface [COM]","IPersistStorage interface [COM]","described","_com_ipersiststorage","com.ipersiststorage","objidl/IPersistStorage"]
old-location: com\ipersiststorage.htm
tech.root: com
ms.assetid: 1c1a20fc-c101-4cbc-a7a6-30613aa387d7
ms.date: 12/05/2018
ms.keywords: IPersistStorage, IPersistStorage interface [COM], IPersistStorage interface [COM],described, _com_ipersiststorage, com.ipersiststorage, objidl/IPersistStorage
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
 - IPersistStorage
 - objidl/IPersistStorage
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
 - IPersistStorage
---

# IPersistStorage interface


## -description

Enables a container application to pass a storage object to one of its contained objects and to load and save the storage object. This interface supports the structured storage model, in which each contained object has its own storage that is nested within the container's storage.

## -inheritance

The <b>IPersistStorage</b> interface inherits from <b>IPersist</b>. <b>IPersistStorage</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/ole/nf-ole-olecreate">OleCreate</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleload">OleLoad</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olesave">OleSave</a>
