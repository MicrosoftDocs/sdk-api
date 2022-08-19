---
UID: NN:objidlbase.IContext
title: IContext (objidlbase.h)
description: The IContext (objidlbase.h) interface supports setting COM+ context properties.
helpviewer_keywords: ["IContext","IContext interface [COM]","IContext interface [COM]","described","_com_icontext","com.icontext","objidlbase/IContext"]
old-location: com\icontext.htm
tech.root: com
ms.assetid: 89c41d9c-186c-4927-990d-92aa501f7d35
ms.date: 08/15/2022
ms.keywords: IContext, IContext interface [COM], IContext interface [COM],described, _com_icontext, com.icontext, objidlbase/IContext
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
 - IContext
 - objidlbase/IContext
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
 - IContext
---

# IContext interface


## -description

Supports setting COM+ context properties.

## -inheritance

The <b>IContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContext</b> also has these types of members:

## -remarks

 An instance of this interface for the current context can be obtained using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetobjectcontext">CoGetObjectContext</a>.
