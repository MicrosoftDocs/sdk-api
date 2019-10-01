---
UID: NF:objidl.IPSFactoryBuffer.CreateProxy
title: IPSFactoryBuffer::CreateProxy (objidl.h)
author: windows-sdk-content
description: Creates a proxy for the specified remote interface.
old-location: com\ipsfactorybuffer_createproxy.htm
tech.root: com
ms.assetid: 7d0638d9-50bc-47f3-8ebd-47bb5cbcab9c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateProxy, CreateProxy method [COM], CreateProxy method [COM],IPSFactoryBuffer interface, IPSFactoryBuffer interface [COM],CreateProxy method, IPSFactoryBuffer.CreateProxy, IPSFactoryBuffer::CreateProxy, _com_ipsfactorybuffer_createproxy, com.ipsfactorybuffer_createproxy, objidlbase/IPSFactoryBuffer::CreateProxy
ms.topic: method
f1_keywords: 
 - "objidl/IPSFactoryBuffer.CreateProxy"
req.header: objidl.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IPSFactoryBuffer.CreateProxy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPSFactoryBuffer::CreateProxy


## -description


Creates a proxy for the specified remote interface.


## -parameters




### -param pUnkOuter [in]

A controlling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface; used for aggregation.


### -param riid [in]

The identifier of the interface to proxy.


### -param ppProxy [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcproxybuffer">IRpcProxyBuffer</a> interface to control marshaling.


### -param ppv [out]

A pointer to the interface specified by <i>riid</i>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> implementation of the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcproxybuffer">IRpcProxyBuffer</a> interface must not delegate to the outer controlling <b>IUnknown</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipsfactorybuffer">IPSFactoryBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irpcproxybuffer">IRpcProxyBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/com/proxy">Proxy</a>
 

 

