---
UID: NN:objidlbase.IComThreadingInfo
title: IComThreadingInfo (objidlbase.h)
description: The IComThreadingInfo (objidlbase.h) interface enables you to obtain the following information about the apartment and thread that the caller is executing.
helpviewer_keywords: ["IComThreadingInfo","IComThreadingInfo interface [COM]","IComThreadingInfo interface [COM]","described","_com_icomthreadinginfo_interface","com.icomthreadinginfo","objidlbase/IComThreadingInfo"]
old-location: com\icomthreadinginfo.htm
tech.root: com
ms.assetid: fa4c7d82-ec5d-43d6-914e-bba60ad19aa2
ms.date: 08/15/2022
ms.keywords: IComThreadingInfo, IComThreadingInfo interface [COM], IComThreadingInfo interface [COM],described, _com_icomthreadinginfo_interface, com.icomthreadinginfo, objidlbase/IComThreadingInfo
req.header: objidlbase.h
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
 - IComThreadingInfo
 - objidlbase/IComThreadingInfo
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
 - IComThreadingInfo
---

# IComThreadingInfo interface


## -description

Enables you to obtain the following information about the apartment and thread that the caller is executing in: apartment type, thread type, and thread GUID. It also allows you to specify a thread GUID.

## -inheritance

The <b>IComThreadingInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComThreadingInfo</b> also has these types of members:

## -remarks

 An instance of this interface for the current context can be obtained using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetobjectcontext">CoGetObjectContext</a>.
