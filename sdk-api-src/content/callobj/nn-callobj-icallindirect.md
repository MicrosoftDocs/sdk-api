---
UID: NN:callobj.ICallIndirect
title: ICallIndirect (callobj.h)
description: Invokes an object with an indirect reference to the invocations arguments, rather than the traditional direct call.
helpviewer_keywords: ["ICallIndirect","ICallIndirect interface [COM]","ICallIndirect interface [COM]","described","_com_icallindirect_interface","callobj/ICallIndirect","com.icallindirect"]
old-location: com\icallindirect.htm
tech.root: com
ms.assetid: b85585fd-5f44-4c07-91a4-145eb44a6bdd
ms.date: 12/05/2018
ms.keywords: ICallIndirect, ICallIndirect interface [COM], ICallIndirect interface [COM],described, _com_icallindirect_interface, callobj/ICallIndirect, com.icallindirect
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
 - ICallIndirect
 - callobj/ICallIndirect
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
 - ICallIndirect
---

# ICallIndirect interface


## -description

Invokes an object with an indirect reference to the invocations arguments, rather than the traditional direct call. An instance of <b>ICallIndirect</b> supports indirect invocations for only one interface ID.

## -inheritance

The <b>ICallIndirect</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICallIndirect</b> also has these types of members:

## -remarks

The actual detailed semantics of how to carry out an indirect call are independent of the <b>ICallIndirect</b> interface itself; they are instead specific to the implementation of the interface. For example, implementations of <b>ICallIndirect</b> found in call interceptors carry out the call by constructing and appropriate <a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a> instance and then invoking <a href="/windows/desktop/api/callobj/nf-callobj-icallframeevents-oncall">ICallFrameEvents::OnCall</a> in the registered sink. Other implementations might do some appropriate munging of the invocations arguments, then forward the call on to some actual specific object, presumably one previously registered with the <b>ICallIndirect</b> using some implementation-specific means.

## -see-also

<a href="/windows/desktop/api/callobj/nn-callobj-icallinterceptor">ICallInterceptor</a>
