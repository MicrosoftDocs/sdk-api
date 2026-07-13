---
UID: NN:callobj.ICallFrame
title: ICallFrame (callobj.h)
description: Enables manipulation of call frames such as stack frames.
helpviewer_keywords: ["ICallFrame","ICallFrame interface [COM]","ICallFrame interface [COM]","described","_com_icallframe_interface","callobj/ICallFrame","com.icallframe"]
old-location: com\icallframe.htm
tech.root: com
ms.assetid: 56a75123-f402-4187-af13-d31f72a5f094
ms.date: 12/05/2018
ms.keywords: ICallFrame, ICallFrame interface [COM], ICallFrame interface [COM],described, _com_icallframe_interface, callobj/ICallFrame, com.icallframe
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
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
 - ICallFrame
 - callobj/ICallFrame
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Callobj.h
api_name:
 - ICallFrame
---

# ICallFrame interface


## -description

Enables manipulation of call frames such as stack frames. The call frame is the body of information that a procedure must save to allow it to properly return to its caller. A call frame may exist on the stack or in registers. A stack frame maintains its caller's context information on the stack.

An instance of the <b>ICallFrame</b> interface can perform various transformations on a call frame. The call can be marshaled or persisted. The instance of this interface is bound and has an associated method number.

## -inheritance

The <b>ICallFrame</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICallFrame</b> also has these types of members:

