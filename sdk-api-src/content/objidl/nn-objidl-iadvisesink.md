---
UID: NN:objidl.IAdviseSink
title: IAdviseSink
author: windows-sdk-content
description: Enables containers and other objects to receive notifications of data changes, view changes, and compound-document changes occurring in objects of interest.
old-location: com\iadvisesink.htm
old-project: com
ms.assetid: bc9f217a-75bd-4155-9d00-df44b00cf0e5
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAdviseSink, IAdviseSink interface [COM], IAdviseSink interface [COM],described, _ole_iadvisesink, com.iadvisesink, objidl/IAdviseSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IAdviseSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IAdviseSink interface


## -description


Enables containers and other objects to receive notifications of data changes, view changes, and compound-document changes occurring in objects of interest. Container applications, for example, require such notifications to keep cached presentations of their linked and embedded objects up-to-date. Calls to <b>IAdviseSink</b> methods are asynchronous, so the call is sent and then the next instruction is executed without waiting for the call's return.

For an advisory connection to exist, the object that is to receive notifications must implement <b>IAdviseSink</b>, and the objects in which it is interested must implement <a href="https://msdn.microsoft.com/6a68c9e9-6e06-4def-89a5-18e184e76a26">IOleObject::Advise</a> and <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a>. In-process objects and handlers may also implement <a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a>. Objects implementing <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> must support all reasonable advisory methods. To simplify advisory notifications, OLE supplies implementations of the <a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a> and <a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a>, which keep track of advisory connections and send notifications to the proper sinks through pointers to their <b>IAdviseSink</b> interfaces. <a href="https://msdn.microsoft.com/4310c987-3542-4a59-a6fb-951143001741">IViewObject</a> (and its advisory methods) is implemented in the default handler.

As shown in the following table, an object that has implemented an advise sink registers its interest in receiving certain types of notifications by calling the appropriate method.
<table>
<tr>
<th>Call This Method</th>
<th> To Register for These Notifications</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6a68c9e9-6e06-4def-89a5-18e184e76a26">IOleObject::Advise</a>
</td>
<td>When a document is saved, closed, or renamed.
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a>
</td>
<td>When a document's data changes.
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a>
</td>
<td>When a document's presentation changes.
</td>
</tr>
</table> 

When an event occurs that applies to a registered notification type, the object application calls the appropriate <b>IAdviseSink</b> method. For example, when an embedded object closes, it calls the <a href="https://msdn.microsoft.com/a695c623-4a4e-4f3d-9f12-ee198c0761a9">IAdviseSink::OnClose</a> method to notify its container. These notifications are asynchronous, occurring after the events that trigger them.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAdviseSink</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IAdviseSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAdviseSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a695c623-4a4e-4f3d-9f12-ee198c0761a9">OnClose</a>
</td>
<td align="left" width="63%">
Advises that the object has been closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">OnDataChange</a>
</td>
<td align="left" width="63%">
Advises that the data has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec9926fb-d69e-430c-b67d-24c52d806bb5">OnRename</a>
</td>
<td align="left" width="63%">
Advises that the name of object has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26da5e16-5790-49c0-ba63-5feee49cd4c6">OnSave</a>
</td>
<td align="left" width="63%">
Advises that the object has been saved to disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2cb3a5b-826b-428a-9e92-e5d08880bddc">OnViewChange</a>
</td>
<td align="left" width="63%">
Advises that the view of object has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/80f55377-8a1e-42b1-8fe0-5896620c8062">IAdviseSink2</a>



<a href="https://msdn.microsoft.com/d1a52353-dd86-4083-9dbc-3a6f363a1a57">IAdviseSinkEx</a>



<a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a>



<a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a>



<a href="https://msdn.microsoft.com/680afee7-2bee-4d54-ae0b-3e4e0deb622f">IOleAdviseHolder</a>



<a href="https://msdn.microsoft.com/6a68c9e9-6e06-4def-89a5-18e184e76a26">IOleObject::Advise</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a>
 

 

