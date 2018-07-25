---
UID: NN:objidl.IDataAdviseHolder
title: IDataAdviseHolder
author: windows-sdk-content
description: Creates and manages advisory connections between a data object and one or more advise sinks.
old-location: com\idataadviseholder.htm
old-project: com
ms.assetid: 740a6366-6ab1-4a20-82df-1efdd62211eb
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IDataAdviseHolder, IDataAdviseHolder interface [COM], IDataAdviseHolder interface [COM],described, _ole_idataadviseholder, com.idataadviseholder, objidl/IDataAdviseHolder
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
 - IDataAdviseHolder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IDataAdviseHolder interface


## -description


Creates and manages advisory connections between a data object and one or more advise sinks. Its methods are intended to be used to implement the advisory methods of <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>. <b>IDataAdviseHolder</b> is implemented on an advise holder object. Its methods establish and delete data advisory connections and send notification of change in data from a data object to an object that requires this notification, such as an OLE container, which must contain an advise sink.

Advise sinks are objects that require notification of change in the data the object contains and implement the <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> interface. Advise sinks are also usually associated with OLE compound document containers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataAdviseHolder</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IDataAdviseHolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDataAdviseHolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b72a50b-a18f-4ec0-9d1d-52b07eb84faf">Advise</a>
</td>
<td align="left" width="63%">
Creates a connection between an advise sink and a data object so the advise sink can receive notification of change in the data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0863d013-6f55-40ce-92d2-68bb0455a911">EnumAdvise</a>
</td>
<td align="left" width="63%">
Returns an object that can be used to enumerate the current advisory connections.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7385116-2ec7-4e12-a2dc-c9029a38d8fd">SendOnDataChange</a>
</td>
<td align="left" width="63%">
Sends a change notification back to each advise sink that is currently being managed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/baeb29fd-1dd2-4320-911d-b271b2250184">Unadvise</a>
</td>
<td align="left" width="63%">
Destroys a notification connection previously set up with the <a href="https://msdn.microsoft.com/3b72a50b-a18f-4ec0-9d1d-52b07eb84faf">Advise</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>



<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>
 

 

