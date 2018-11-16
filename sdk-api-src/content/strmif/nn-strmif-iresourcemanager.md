---
UID: NN:strmif.IResourceManager
title: IResourceManager
author: windows-sdk-content
description: The IResourceManager interface resolves contentions for system resources.The filter graph manager exposes this interface.
old-location: dshow\iresourcemanager.htm
tech.root: DirectShow
ms.assetid: 8cbe908e-5675-4134-81e7-2c5c31b0ffc5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IResourceManager, IResourceManager interface [DirectShow], IResourceManager interface [DirectShow],described, IResourceManagerInterface, dshow.iresourcemanager, strmif/IResourceManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IResourceManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResourceManager interface


## -description



The <code>IResourceManager</code> interface resolves contentions for system resources.

The filter graph manager exposes this interface. Filters can use this interface to request resources that other objects are likely to use. For example, audio renderers use this interface to resolve contentions for the wave-output device, to enable sound to follow focus.

Applications will typically not use this interface.

An object can use this interface to resolve possible contentions between existing resources. The object registers the resource with the interface and then requests it whenever needed. The object should notify the filter graph manager whenever the user focus changes. The filter graph manager can then switch contended resources to the objects that have the focus of the user.

An object that uses this interface must implement the <a href="https://msdn.microsoft.com/dda2b207-dcd8-42df-95a3-d4bfbb4a7fd8">IResourceConsumer</a> interface. <b>IResourceConsumer</b> provides a callback mechanism for the filter graph manager to notify the object when a resource becomes available, or when the object should release a resource that it acquired.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResourceManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IResourceManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IResourceManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49372654-8e69-4a7a-915e-16e791c63fb2">CancelRequest</a>
</td>
<td align="left" width="63%">
Cancels the request for a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5c52f5b-1c21-4f4c-b698-15b6ec7f7fed">NotifyAcquire</a>
</td>
<td align="left" width="63%">
Notifies the resource manager that an attempt to acquire a resource has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3779a8d-fe78-4f9b-af6c-7a25e0f07a86">NotifyRelease</a>
</td>
<td align="left" width="63%">
Notifies the resource manager that a resource consumer has released a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23fa6830-144b-479f-8a8e-b637d82f51d1">Register</a>
</td>
<td align="left" width="63%">
Registers a single named resource with the resource manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2d3deb2-8f22-42ac-846c-2f158f347ca7">RegisterGroup</a>
</td>
<td align="left" width="63%">
Registers a named resource group with the resource manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfc1b178-eb81-488b-8a4a-f1a454b3d5f4">ReleaseFocus</a>
</td>
<td align="left" width="63%">
Sets the focus object to <b>NULL</b> in the resource manager if the object of the current focus object is the one specified in this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b52dc38a-9246-4cef-ba1a-cf1927223183">RequestResource</a>
</td>
<td align="left" width="63%">
Requests the use of a given registered resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d0a87e1-6774-45cf-9ab5-18ec1d2fff0d">SetFocus</a>
</td>
<td align="left" width="63%">
Notifies the resource manager that a specified object has been given the focus of the user.

</td>
</tr>
</table> 

