---
UID: NN:objidl.IPersist
title: IPersist (objidl.h)
author: windows-sdk-content
description: Provides the CLSID of an object that can be stored persistently in the system. Allows the object to specify which object handler to use in the client process, as it is used in the default implementation of marshaling.
old-location: com\ipersist.htm
tech.root: com
ms.assetid: 932eb0e2-35a6-482e-9138-00cff30508a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPersist, IPersist interface [COM], IPersist interface [COM],described, _com_ipersist, com.ipersist, objidl/IPersist
ms.topic: interface
f1_keywords: ["objidl/IPersist"]
req.header: objidl.h
req.include-header: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IPersist
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPersist interface


## -description


Provides the CLSID of an object that can be stored persistently in the system. Allows the object to specify which object handler to use in the client process, as it is used in the default implementation of marshaling.

<b>IPersist</b> is the base interface for three other interfaces: <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>, <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>. Each of these interfaces, therefore, includes the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">GetClassID</a> method, and the appropriate one of these three interfaces is implemented on objects that can be serialized to a storage, a stream, or a file. The methods of these interfaces allow the state of these objects to be saved for later instantiations, and load the object using the saved state. Typically, the persistence interfaces are implemented by an embedded or linked object, and are called by the container application or the default object handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersist</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPersist</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersist</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid">GetClassID</a>
</td>
<td align="left" width="63%">
Retrieves the class identifier (CLSID) of the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>
 

 

