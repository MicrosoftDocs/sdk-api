---
UID: NN:upnp.IUPnPServiceAsync
title: IUPnPServiceAsync
author: windows-sdk-content
description: Use this interface to asynchronously query state variables and invoke actions on an instance of a service .
old-location: upnp\iupnpserviceasync.htm
old-project: upnp
ms.assetid: B77025D6-26C7-46C9-84FE-69685C61735D
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: IUPnPServiceAsync, IUPnPServiceAsync interface [UPnP APIs], IUPnPServiceAsync interface [UPnP APIs],described, upnp.iupnpserviceasync, upnp/IUPnPServiceAsync
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: upnp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPServiceAsync interface


## -description


Use this interface to asynchronously query state variables and invoke actions on an instance of a service .

This interface can be obtained through a <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> off the <a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPServiceAsync</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPServiceAsync</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPServiceAsync</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40900CE1-03EE-451A-84DE-5C496EB2D7E5">BeginInvokeAction</a>
</td>
<td align="left" width="63%">
Invokes an action on a device in asynchronous mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1E97589C-A06B-4012-A2A2-C88BBE9B2530">BeginQueryStateVariable</a>
</td>
<td align="left" width="63%">
Initiates a request for the state variable value for a specific service in asynchronous mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CA573855-6D86-4C6C-B557-F8E8776BDBD3">BeginSCPDDownload</a>
</td>
<td align="left" width="63%">
Initiates asynchronous download of the Service Control Protocol Description (SCPD) document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/605629CB-9DBA-4130-B55D-957187551435">BeginSubscribeToEvents</a>
</td>
<td align="left" width="63%">
Initiates the registration of an application callback with the UPnP framework in asynchronous mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FBEC2DF3-6D45-49F2-AAA8-6DED697BC5A6">CancelAsyncOperation</a>
</td>
<td align="left" width="63%">
Cancels any asynchronous operation initiated by the <a href="https://msdn.microsoft.com/40900CE1-03EE-451A-84DE-5C496EB2D7E5">BeginInvokeAction</a>, <a href="https://msdn.microsoft.com/1E97589C-A06B-4012-A2A2-C88BBE9B2530">BeginQueryStateVariable</a>, <a href="https://msdn.microsoft.com/605629CB-9DBA-4130-B55D-957187551435">BeginSubscribeToEvents</a>, or <a href="https://msdn.microsoft.com/CA573855-6D86-4C6C-B557-F8E8776BDBD3">BeginSCPDDownload</a> methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1B10F8E9-D3C9-432B-B773-77B4BB82224C">EndInvokeAction</a>
</td>
<td align="left" width="63%">
Finalizes a <a href="https://msdn.microsoft.com/40900CE1-03EE-451A-84DE-5C496EB2D7E5">BeginInvokeAction</a> operation and retrieves the resultant output arguments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82AAB2C4-46A9-4545-95E1-887841735815">EndQueryStateVariable</a>
</td>
<td align="left" width="63%">
Retrieves the service state variable value requested by <a href="https://msdn.microsoft.com/1E97589C-A06B-4012-A2A2-C88BBE9B2530">BeginQueryStateVariable</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1C4F7986-9282-4775-B9B2-338AC44F2243">EndSPCDDownload</a>
</td>
<td align="left" width="63%">
Finalizes asynchronous download of the Service Control Protocol Description (SCPD) document initiated by <a href="https://msdn.microsoft.com/CA573855-6D86-4C6C-B557-F8E8776BDBD3">BeginSCPDDownload</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A0C0D01C-3A05-4498-9235-CBBF7D5D558F">EndSubscribeToEvents</a>
</td>
<td align="left" width="63%">
Finalizes the <a href="https://msdn.microsoft.com/605629CB-9DBA-4130-B55D-957187551435">BeginSubscribeToEvents</a> operation. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/53854510-BB0C-41E6-8651-F34991B24D5E">IUPnPAsyncResult</a>
 

 

