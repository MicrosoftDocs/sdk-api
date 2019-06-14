---
UID: NN:unknwnbase.IClassFactory
title: IClassFactory (unknwnbase.h)
author: windows-sdk-content
description: Enables a class of objects to be created.
old-location: com\iclassfactory.htm
tech.root: com
ms.assetid: f624f833-2b69-43bc-92cd-c4ecbe6051c5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IClassFactory, IClassFactory interface [COM], IClassFactory interface [COM],described, _com_iclassfactory, com.iclassfactory, unknwnbase/IClassFactory
ms.topic: interface
req.header: unknwnbase.h
req.include-header: Unknwn.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Unknwn.idl
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
 - unknwnbase.h
api_name:
 - IClassFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IClassFactory interface


## -description


Enables a class of objects to be created.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IClassFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IClassFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IClassFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iclassfactory-createinstance">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an uninitialized object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/unknwnbase/nf-unknwnbase-iclassfactory-lockserver">LockServer</a>
</td>
<td align="left" width="63%">
Locks an object application open in memory.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject">CoGetClassObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ole/nf-ole-olecreate">OleCreate</a>
 

 

