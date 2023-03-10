---
UID: NN:objidl.IGlobalInterfaceTable
title: IGlobalInterfaceTable (objidl.h)
description: Enables any apartment in a process to get access to an interface implemented on an object in any other apartment in the process.
helpviewer_keywords: ["IGlobalInterfaceTable","IGlobalInterfaceTable interface [COM]","IGlobalInterfaceTable interface [COM]","described","_com_iglobalinterfacetable","com.iglobalinterfacetable","objidl/IGlobalInterfaceTable"]
old-location: com\iglobalinterfacetable.htm
tech.root: com
ms.assetid: 0c1feee7-e33b-4b5d-8e35-4de6895e3947
ms.date: 12/05/2018
ms.keywords: IGlobalInterfaceTable, IGlobalInterfaceTable interface [COM], IGlobalInterfaceTable interface [COM],described, _com_iglobalinterfacetable, com.iglobalinterfacetable, objidl/IGlobalInterfaceTable
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
 - IGlobalInterfaceTable
 - objidl/IGlobalInterfaceTable
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
 - IGlobalInterfaceTable
---

# IGlobalInterfaceTable interface


## -description

Enables any apartment in a process to get access to an interface implemented on an object in any other apartment in the process.

## -inheritance

The <b>IGlobalInterfaceTable</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGlobalInterfaceTable</b> also has these types of members:

## -remarks

The <b>IGlobalInterfaceTable</b> interface is an efficient way for a process to store an interface pointer in a memory location that can be accessed from multiple apartments within the process, such as processwide variables and agile (free-threaded marshaled) objects containing interface pointers to other objects. 



An agile object is unaware of the underlying COM infrastructure in which it runs - in other words, what apartment, context, and thread it is executing on. The object may be holding on to interfaces that are specific to an apartment or context. For this reason, calling these interfaces from wherever the agile component is executing may not always work properly. The global interface table avoids this problem by guaranteeing that a valid proxy (or direct pointer) to the object is used, based on where the agile object is executing.

The global interface table is not portable across process or machine boundaries, so it cannot be used in place of the normal parameter-passing mechanism.
