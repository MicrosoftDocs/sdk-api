---
UID: NN:objidlbase.IPSFactoryBuffer
title: IPSFactoryBuffer (objidlbase.h)
description: Provides custom methods for the creation of COM object proxies and stubs. This interface is not marshalable.
helpviewer_keywords: ["IPSFactoryBuffer","IPSFactoryBuffer interface [COM]","IPSFactoryBuffer interface [COM]","described","_com_ipsfactorybuffer","com.ipsfactorybuffer","objidlbase/IPSFactoryBuffer"]
old-location: com\ipsfactorybuffer.htm
tech.root: com
ms.assetid: ffe85701-a4fa-4cf3-9b86-85f3a0cb63e9
ms.date: 12/05/2018
ms.keywords: IPSFactoryBuffer, IPSFactoryBuffer interface [COM], IPSFactoryBuffer interface [COM],described, _com_ipsfactorybuffer, com.ipsfactorybuffer, objidlbase/IPSFactoryBuffer
f1_keywords:
- objidlbase/IPSFactoryBuffer
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- objidlbase.h
api_name:
- IPSFactoryBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPSFactoryBuffer interface


## -description


Provides custom methods for the creation of COM object proxies and stubs. This interface is not marshalable.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPSFactoryBuffer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPSFactoryBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPSFactoryBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipsfactorybuffer-createproxy">CreateProxy</a>
</td>
<td align="left" width="63%">
Creates a proxy for the specified remote interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipsfactorybuffer-createstub">CreateStub</a>
</td>
<td align="left" width="63%">
Creates a stub for the remote use of the specified interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>



<a href="https://docs.microsoft.com/windows/desktop/com/proxy">Proxy</a>



<a href="https://docs.microsoft.com/windows/desktop/com/stub">Stub</a>
 

 

