---
UID: NN:ctxtcall.IContextCallback
title: IContextCallback (ctxtcall.h)
description: Provides a mechanism to execute a function inside a specific COM+ object context.
helpviewer_keywords: ["IContextCallback","IContextCallback interface [COM]","IContextCallback interface [COM]","described","_com_icontextcallback","com.icontextcallback","ctxtcall/IContextCallback"]
old-location: com\icontextcallback.htm
tech.root: com
ms.assetid: 47af7b80-3419-4a40-8932-a5a27f297dc9
ms.date: 12/05/2018
ms.keywords: IContextCallback, IContextCallback interface [COM], IContextCallback interface [COM],described, _com_icontextcallback, com.icontextcallback, ctxtcall/IContextCallback
req.header: ctxtcall.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctxtcall.idl
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
 - IContextCallback
 - ctxtcall/IContextCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctxtcall.h
api_name:
 - IContextCallback
---

# IContextCallback interface


## -description

Provides a mechanism to execute a function inside a specific COM+ object context.

## -inheritance

The <b>IContextCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContextCallback</b> also has these types of members:

## -remarks

 An instance of this interface for the current context can be obtained using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetobjectcontext">CoGetObjectContext</a>.
