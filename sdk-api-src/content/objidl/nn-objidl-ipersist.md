---
UID: NN:objidl.IPersist
title: IPersist
author: windows-sdk-content
description: Provides the CLSID of an object that can be stored persistently in the system. Allows the object to specify which object handler to use in the client process, as it is used in the default implementation of marshaling.
old-location: com\ipersist.htm
old-project: com
ms.assetid: 932eb0e2-35a6-482e-9138-00cff30508a9
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IPersist, IPersist interface [COM], IPersist interface [COM],described, _com_ipersist, com.ipersist, objidl/IPersist
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: THDTYPE
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
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IPersist interface


## -description


Provides the CLSID of an object that can be stored persistently in the system. Allows the object to specify which object handler to use in the client process, as it is used in the default implementation of marshaling.

<b>IPersist</b> is the base interface for three other interfaces: <a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a>, <a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>, and <a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a>. Each of these interfaces, therefore, includes the <a href="https://msdn.microsoft.com/921a3b86-a240-454e-9411-8d653e02b90e">GetClassID</a> method, and the appropriate one of these three interfaces is implemented on objects that can be serialized to a storage, a stream, or a file. The methods of these interfaces allow the state of these objects to be saved for later instantiations, and load the object using the saved state. Typically, the persistence interfaces are implemented by an embedded or linked object, and are called by the container application or the default object handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersist</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IPersist</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/921a3b86-a240-454e-9411-8d653e02b90e">GetClassID</a>
</td>
<td align="left" width="63%">
Retrieves the class identifier (CLSID) of the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7d34507f-8a16-43b4-8225-010798abc546">IPersistFile</a>



<a href="https://msdn.microsoft.com/1c1a20fc-c101-4cbc-a7a6-30613aa387d7">IPersistStorage</a>



<a href="https://msdn.microsoft.com/97ea64ee-d950-4872-add6-1f532a6eb33f">IPersistStream</a>
 

 

