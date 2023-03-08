---
UID: NN:objidl.IClientSecurity
title: IClientSecurity (objidl.h)
description: Gives the client control over the security settings for each individual interface proxy of an object.
helpviewer_keywords: ["IClientSecurity","IClientSecurity interface [COM]","IClientSecurity interface [COM]","described","_com_iclientsecurity","com.iclientsecurity","objidl/IClientSecurity"]
old-location: com\iclientsecurity.htm
tech.root: com
ms.assetid: 65066913-f9d8-48c7-bcb5-68c8ddc4a009
ms.date: 12/05/2018
ms.keywords: IClientSecurity, IClientSecurity interface [COM], IClientSecurity interface [COM],described, _com_iclientsecurity, com.iclientsecurity, objidl/IClientSecurity
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
 - IClientSecurity
 - objidl/IClientSecurity
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
 - IClientSecurity
---

# IClientSecurity interface


## -description

Gives the client control over the security settings for each individual interface proxy of an object.

## -inheritance

The <b>IClientSecurity</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IClientSecurity</b> also has these types of members:

## -remarks

Every object has one proxy manager, and every proxy manager exposes the <b>IClientSecurity</b> interface automatically. Therefore, the client can query the proxy manager of an object for <b>IClientSecurity</b>, using any interface pointer on the object. If the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> call succeeds, the <b>IClientSecurity</b> pointer can be used to call an <b>IClientSecurity</b> method, passing a pointer to the interface proxy that the client is interested in. If a call to <b>QueryInterface</b> for <b>IClientSecurity</b> fails, either the object is implemented in-process or it is remoted by a custom marshaler that does not support security. (A custom marshaler can support security by offering the <b>IClientSecurity</b> interface to the client.)

The interface proxies passed as parameters to <b>IClientSecurity</b> methods must be from the same object as the <b>IClientSecurity</b> interface. That is, each object has a distinct <b>IClientSecurity</b> interface; calling <b>IClientSecurity</b> on one object and passing a proxy to another object will not work. Also, you cannot pass an interface to an <b>IClientSecurity</b> method if the interface does not use a proxy. This means that interfaces implemented locally by the proxy manager cannot be passed to <b>IClientSecurity</b> methods, except for <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, which is the exception to this rule.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>



<a href="/windows/desktop/com/security-in-com">Security in COM</a>



<a href="/windows/desktop/com/setting-processwide-security-with-coinitializesecurity">Setting Process-Wide Security with CoInitializeSecurity</a>
