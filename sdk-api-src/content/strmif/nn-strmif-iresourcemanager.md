---
UID: NN:strmif.IResourceManager
title: IResourceManager (strmif.h)
author: windows-sdk-content
description: The IResourceManager interface resolves contentions for system resources.The filter graph manager exposes this interface.
old-location: dshow\iresourcemanager.htm
tech.root: DirectShow
ms.assetid: 8cbe908e-5675-4134-81e7-2c5c31b0ffc5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IResourceManager, IResourceManager interface [DirectShow], IResourceManager interface [DirectShow],described, IResourceManagerInterface, dshow.iresourcemanager, strmif/IResourceManager
ms.topic: interface
f1_keywords: 
 - "strmif/IResourceManager"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IResourceManager interface


## -description



The <code>IResourceManager</code> interface resolves contentions for system resources.

The filter graph manager exposes this interface. Filters can use this interface to request resources that other objects are likely to use. For example, audio renderers use this interface to resolve contentions for the wave-output device, to enable sound to follow focus.

Applications will typically not use this interface.

An object can use this interface to resolve possible contentions between existing resources. The object registers the resource with the interface and then requests it whenever needed. The object should notify the filter graph manager whenever the user focus changes. The filter graph manager can then switch contended resources to the objects that have the focus of the user.

An object that uses this interface must implement the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iresourceconsumer">IResourceConsumer</a> interface. <b>IResourceConsumer</b> provides a callback mechanism for the filter graph manager to notify the object when a resource becomes available, or when the object should release a resource that it acquired.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResourceManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IResourceManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iresourcemanager-cancelrequest">CancelRequest</a>
</td>
<td align="left" width="63%">
Cancels the request for a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iresourcemanager-notifyacquire">NotifyAcquire</a>
</td>
<td align="left" width="63%">
Notifies the resource manager that an attempt to acquire a resource has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iresourcemanager-notifyrelease">NotifyRelease</a>
</td>
<td align="left" width="63%">
Notifies the resource manager that a resource consumer has released a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iresourcemanager-register">Register</a>
</td>
<td align="left" width="63%">
Registers a single named resource with the resource manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iresourcemanager-registergroup">RegisterGroup</a>
</td>
<td align="left" width="63%">
Registers a named resource group with the resource manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iresourcemanager-releasefocus">ReleaseFocus</a>
</td>
<td align="left" width="63%">
Sets the focus object to <b>NULL</b> in the resource manager if the object of the current focus object is the one specified in this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iresourcemanager-requestresource">RequestResource</a>
</td>
<td align="left" width="63%">
Requests the use of a given registered resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iresourcemanager-setfocus">SetFocus</a>
</td>
<td align="left" width="63%">
Notifies the resource manager that a specified object has been given the focus of the user.

</td>
</tr>
</table> 

