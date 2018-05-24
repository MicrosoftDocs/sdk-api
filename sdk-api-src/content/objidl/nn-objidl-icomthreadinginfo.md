---
UID: NN:objidl.IComThreadingInfo
title: IComThreadingInfo
author: windows-driver-content
description: Enables you to obtain the following information about the apartment and thread that the caller is executing in:\_apartment type, thread type, and thread GUID. It also allows you to specify a thread GUID.
old-location: com\icomthreadinginfo.htm
old-project: com
ms.assetid: fa4c7d82-ec5d-43d6-914e-bba60ad19aa2
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IComThreadingInfo, IComThreadingInfo interface [COM], IComThreadingInfo interface [COM],described, _com_icomthreadinginfo_interface, com.icomthreadinginfo, objidlbase/IComThreadingInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IComThreadingInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IComThreadingInfo interface


## -description


Enables you to obtain the following information about the apartment and thread that the caller is executing in: apartment type, thread type, and thread GUID. It also allows you to specify a thread GUID.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComThreadingInfo</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IComThreadingInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComThreadingInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59cb216f-818c-4189-b77b-984961889a62">GetCurrentApartmentType</a>
</td>
<td align="left" width="63%">
Retrieves the type of apartment in which the caller is executing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/780bc94d-19b6-4cc8-b27f-9e38520b0afc">GetCurrentLogicalThreadId</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the thread in which the caller is executing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93437e45-f1e7-4f1f-bffb-ef234c7f5a6b">GetCurrentThreadType</a>
</td>
<td align="left" width="63%">
Retrieves the type of thread in which the caller is executing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a2fb319-094e-4384-b520-2cb8b8819d42">SetCurrentLogicalThreadId</a>
</td>
<td align="left" width="63%">
Sets the GUID of the thread in which the caller is executing.

</td>
</tr>
</table> 


## -remarks



 An instance of this interface for the current context can be obtained using <a href="https://msdn.microsoft.com/97a0c6c3-a011-44dc-b428-aabdad7d4364">CoGetObjectContext</a>.



