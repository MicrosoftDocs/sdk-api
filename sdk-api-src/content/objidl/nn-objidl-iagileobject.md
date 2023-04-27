---
UID: NN:objidl.IAgileObject
title: IAgileObject (objidl.h)
description: The IAgileObject interface (objidl.h) marks an interface as agile across apartments.
helpviewer_keywords: ["IAgileObject","IAgileObject interface [COM]","IAgileObject interface [COM]","described","com.iagileobject","objidl/IAgileObject"]
old-location: com\iagileobject.htm
tech.root: com
ms.assetid: 787A22DE-AEAB-4570-BB97-C49D656E5D40
ms.date: 08/15/2022
ms.keywords: IAgileObject, IAgileObject interface [COM], IAgileObject interface [COM],described, com.iagileobject, objidl/IAgileObject
req.header: objidl.h
req.include-header: Objidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
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
 - IAgileObject
 - objidl/IAgileObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidl.h
api_name:
 - IAgileObject
---

# IAgileObject interface


## -description

Marks an interface as agile across apartments.

## -remarks

The <b>IAgileObject</b> interface is a marker interface that indicates that an object is free threaded and can be called from any apartment.

Unlike what happens when aggregating the Free Threaded Marshaler (FTM), implementing the <b>IAgileObject</b> interface doesn't affect what happens when marshaling a call. Instead, the <b>IAgileObject</b> interface is recognized by the Global Interface Table (GIT). When an object that implements the <b>IAgileObject</b> interface is placed in the GIT and localized to another apartment, the object is called directly in the new apartment, rather than marshaling.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
