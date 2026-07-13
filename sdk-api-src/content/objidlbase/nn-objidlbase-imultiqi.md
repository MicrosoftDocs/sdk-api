---
UID: NN:objidlbase.IMultiQI
title: IMultiQI (objidlbase.h)
description: The IMultiQI (objidlbase.h) interface enables a client to query an object proxy, or handler, for multiple interfaces by using a single RPC call.
helpviewer_keywords: ["IMultiQI","IMultiQI interface [COM]","IMultiQI interface [COM]","described","_com_imultiqi","com.imultiqi","objidlbase/IMultiQI"]
old-location: com\imultiqi.htm
tech.root: com
ms.assetid: 5e50396f-2931-403f-946a-dc096cb012cc
ms.date: 08/15/2022
ms.keywords: IMultiQI, IMultiQI interface [COM], IMultiQI interface [COM],described, _com_imultiqi, com.imultiqi, objidlbase/IMultiQI
req.header: objidlbase.h
req.include-header: ObjIdl.h
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
 - IMultiQI
 - objidlbase/IMultiQI
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
 - IMultiQI
---

# IMultiQI interface


## -description

Enables a client to query an object proxy, or handler, for multiple interfaces by using a single RPC call. By using this interface, instead of relying on separate calls to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>, clients can reduce the number of RPC calls that have to cross thread, process, or machine boundaries and, therefore, the amount of time required to obtain the requested interface pointers.

## -inheritance

The <b>IMultiQI</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMultiQI</b> also has these types of members:

