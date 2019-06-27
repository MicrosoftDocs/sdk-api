---
UID: NN:objidl.ISynchronizeEvent
title: ISynchronizeEvent (objidl.h)
author: windows-sdk-content
description: Assigns an event handle to a synchronization object.
old-location: com\isynchronizeevent.htm
tech.root: com
ms.assetid: b4721498-0455-415a-bf2f-c8c8fdf3b75c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISynchronizeEvent, ISynchronizeEvent interface [COM], ISynchronizeEvent interface [COM],described, _com_isynchronizeevent, com.isynchronizeevent, objidlbase/ISynchronizeEvent
ms.topic: interface
f1_keywords: 
 - "objidl/ISynchronizeEvent"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ISynchronizeEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISynchronizeEvent interface


## -description


Assigns an event handle to a synchronization object.

The synchronization object can use a handle to manage its activities. For example, the <a href="https://docs.microsoft.com/windows/desktop/Sync/wait-functions">wait functions</a> use handles to identify the event they control. Thus, the logic of the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isynchronize-signal">ISynchronize::Signal</a> method on an event synchronization object can pass its handle to the <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISynchronizeEvent</b> interface inherits from <b>ISynchronizeHandle</b>. <b>ISynchronizeEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISynchronizeEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isynchronizeevent-seteventhandle">SetEventHandle</a>
</td>
<td align="left" width="63%">
Assigns an event handle to a synchronization object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-isynchronizehandle">ISynchronizeHandle</a>
 

 

