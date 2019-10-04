---
UID: NN:objidl.IMultiQI
title: IMultiQI (objidl.h)
author: windows-sdk-content
description: Enables a client to query an object proxy, or handler, for multiple interfaces by using a single RPC call.
old-location: com\imultiqi.htm
tech.root: com
ms.assetid: 5e50396f-2931-403f-946a-dc096cb012cc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMultiQI, IMultiQI interface [COM], IMultiQI interface [COM],described, _com_imultiqi, com.imultiqi, objidlbase/IMultiQI
ms.topic: interface
f1_keywords: 
 - "objidl/IMultiQI"
dev_langs:
 - c++
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
 - IMultiQI
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMultiQI interface


## -description


Enables a client to query an object proxy, or handler, for multiple interfaces by using a single RPC call. By using this interface, instead of relying on separate calls to <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a>, clients can reduce the number of RPC calls that have to cross thread, process, or machine boundaries and, therefore, the amount of time required to obtain the requested interface pointers.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMultiQI</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMultiQI</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMultiQI</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-imultiqi-querymultipleinterfaces">QueryMultipleInterfaces</a>
</td>
<td align="left" width="63%">
Retrieves pointers to multiple supported interfaces on an object.

</td>
</tr>
</table> 

