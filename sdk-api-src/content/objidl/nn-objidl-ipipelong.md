---
UID: NN:objidl.IPipeLong
title: IPipeLong (objidl.h)
description: The IPipeLong interface (objidl.h) transfers data of the long integer type, which is 32 bits wide. 
helpviewer_keywords: ["IPipeLong","IPipeLong interface [COM]","IPipeLong interface [COM]","described","_com_ipipelong","com.ipipelong","objidlbase/IPipeLong"]
old-location: com\ipipelong.htm
tech.root: com
ms.assetid: c1b4d3b3-e1bf-4441-8cea-b667b82c4c27
ms.date: 08/15/2022
ms.keywords: IPipeLong, IPipeLong interface [COM], IPipeLong interface [COM],described, _com_ipipelong, com.ipipelong, objidlbase/IPipeLong
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
 - IPipeLong
 - objidl/IPipeLong
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
 - IPipeLong
---

# IPipeLong interface


## -description

Transfers data of the long integer type (which is 32 bits wide).

## -inheritance

The <b>IPipeLong</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPipeLong</b> also has these types of members:

## -remarks

The <a href="/windows/desktop/api/objidl/nn-objidl-ipipebyte">IPipeByte</a>, <a href="/windows/desktop/api/objidl/nn-objidl-ipipedouble">IPipeDouble</a>, and <b>IPipeLong</b> interfaces are similar to the standard DCE/RPC pipes. However, the COM implementation of pipes offers more flexibility. With the COM implementation, the basic idea is that the pipe is simply another interface with two methods: <a href="/windows/desktop/api/objidl/nf-objidl-ipipelong-pull">Pull</a> and <a href="/windows/desktop/api/objidl/nf-objidl-ipipelong-push">Push</a>. This results in three main benefits: 



<ul>
<li>A COM pipe is another interface, so it can be received as an out parameter from a method call and then either <a href="/windows/desktop/api/objidl/nf-objidl-ipipelong-pull">Pull</a> or <a href="/windows/desktop/api/objidl/nf-objidl-ipipelong-push">Push</a> can be called. </li>
<li>There are no restrictions on when to call the <a href="/windows/desktop/api/objidl/nf-objidl-ipipelong-pull">Pull</a> and <a href="/windows/desktop/api/objidl/nf-objidl-ipipelong-push">Push</a> methods, so a pipe is in reality bidirectional. 
</li>
<li>Pipes are interfaces, so the method calls can be asynchronous and follow those rules.</li>
</ul>
For more information, see <a href="/windows/desktop/Rpc/pipes">Pipes</a> in the RPC documentation.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipipebyte">IPipeByte</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ipipedouble">IPipeDouble</a>
