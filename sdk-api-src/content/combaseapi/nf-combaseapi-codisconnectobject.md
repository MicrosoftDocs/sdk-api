---
UID: NF:combaseapi.CoDisconnectObject
title: CoDisconnectObject function
author: windows-sdk-content
description: Disconnects all remote process connections being maintained on behalf of all the interface pointers that point to a specified object.
old-location: com\codisconnectobject.htm
tech.root: com
ms.assetid: 4293316a-bafe-4fca-ad6a-68d8e99c8fba
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: CoDisconnectObject, CoDisconnectObject function [COM], _com_CoDisconnectObject, com.codisconnectobject, combaseapi/CoDisconnectObject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoDisconnectObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoDisconnectObject function


## -description


Disconnects all remote process connections being maintained on behalf of all the interface pointers that point to a specified object.

Only the process that actually manages the object should call <b>CoDisconnectObject</b>.


## -parameters




### -param pUnk [in]

A pointer to any interface derived from <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> on the object to be disconnected.


### -param dwReserved [in]

This parameter is reserved and must be 0.


## -returns



This function returns S_OK to indicate that all connections to remote processes were successfully deleted.




## -remarks



The <b>CoDisconnectObject</b> function enables a server to correctly disconnect all external clients to the object specified by <i>pUnk</i>.

It performs the following tasks:

<ol>
<li>Checks to see whether the object to be disconnected implements the <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> interface. If so, it gets the pointer to that interface; if not, it gets a pointer to the standard marshaler's (i.e., COM's) <b>IMarshal</b> implementation.</li>
<li>Using whichever <a href="https://msdn.microsoft.com/e6f08949-f27d-4aba-adff-eaf9c356a928">IMarshal</a> interface pointer it has acquired, the function then calls <a href="https://msdn.microsoft.com/1a087fe2-d1ad-4ed9-b6f2-12389656e384">IMarshal::DisconnectObject</a> to disconnect all out-of-process clients.</li>
</ol>
An object's client does not call <b>CoDisconnectObject</b> to disconnect itself from the server (clients should use <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> for this purpose). Rather, an OLE server calls <b>CoDisconnectObject</b> to forcibly disconnect an object's clients, usually in response to a user closing the server application.

Similarly, an OLE container that supports external links to its embedded objects can call <b>CoDisconnectObject</b> to destroy those links. Again, this call is normally made in response to a user closing the application. The container should first call <a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a> for all its OLE objects, each of which should send <a href="https://msdn.microsoft.com/a695c623-4a4e-4f3d-9f12-ee198c0761a9">IAdviseSink::OnClose</a> notifications to their various clients. Then the container can call <b>CoDisconnectObject</b> to close any existing connections.



<b>CoDisconnectObject</b> does not necessarily disconnect out-of-process clients immediately. If any marshaled calls are pending on the server object, <b>CoDisconnectObject</b> disconnects the object only when those calls have returned. In the meantime, <b>CoDisconnectObject</b> sets a flag that causes any new marshaled calls to return CO_E_OBJNOTCONNECTED.





## -see-also




<a href="https://msdn.microsoft.com/a695c623-4a4e-4f3d-9f12-ee198c0761a9">IAdviseSink::OnClose</a>



<a href="https://msdn.microsoft.com/1a087fe2-d1ad-4ed9-b6f2-12389656e384">IMarshal::DisconnectObject</a>



<a href="https://msdn.microsoft.com/61ecd153-ed6b-4a2c-a862-54742c5769ee">IOleObject::Close</a>
 

 

