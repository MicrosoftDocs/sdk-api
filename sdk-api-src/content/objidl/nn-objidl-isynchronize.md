---
UID: NN:objidl.ISynchronize
title: ISynchronize (objidl.h)
description: The ISynchronize (objidl.h) interface provides asynchronous communication between objects about the occurrence of an event.
helpviewer_keywords: ["ISynchronize","ISynchronize interface [COM]","ISynchronize interface [COM]","described","_com_isynchronize","com.isynchronize","objidlbase/ISynchronize"]
old-location: com\isynchronize.htm
tech.root: com
ms.assetid: 2c1e3d27-abb4-4bd0-ad9e-4dc9eda8e4b6
ms.date: 08/13/2022
ms.keywords: ISynchronize, ISynchronize interface [COM], ISynchronize interface [COM],described, _com_isynchronize, com.isynchronize, objidlbase/ISynchronize
req.header: objidl.h
req.include-header: ObjIdl.h
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
 - ISynchronize
 - objidl/ISynchronize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ISynchronize
---

# ISynchronize interface


## -description

Provides asynchronous communication between objects about the occurrence of an event. Objects that implement <b>ISynchronize</b> can receive indications that an event has occurred, and they can respond to queries about the event. In this way, clients can make sure that one request has been processed before they submit a subsequent request that depends on completion of the first one.

## -inheritance

The <b>ISynchronize</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISynchronize</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-isynchronizecontainer">ISynchronizeContainer</a>
