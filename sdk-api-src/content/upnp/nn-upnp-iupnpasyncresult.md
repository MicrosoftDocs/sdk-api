---
UID: NN:upnp.IUPnPAsyncResult
title: IUPnPAsyncResult
author: windows-sdk-content
description: The IUPnPAsyncResult interface is used to notify the UPnP control point of a completed asynchronous I/O operation.
old-location: upnp\iupnpasyncresult.htm
old-project: upnp
ms.assetid: 53854510-BB0C-41E6-8651-F34991B24D5E
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IUPnPAsyncResult, IUPnPAsyncResult interface [UPnP APIs], IUPnPAsyncResult interface [UPnP APIs],described, upnp.iupnpasyncresult, upnp/IUPnPAsyncResult
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: upnp.h
req.include-header: 
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
 - IUPnPAsyncResult
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPAsyncResult interface


## -description


The 
<a href="https://msdn.microsoft.com/44515be4-891b-4f3d-a2c2-1699e468e708">IUPnPAsyncResult</a> interface is used to notify the UPnP control point of a completed asynchronous I/O operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPAsyncResult</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPAsyncResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPAsyncResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C71C0A78-C3D1-4725-99E2-542786B03C8F">AsyncOperationComplete</a>
</td>
<td align="left" width="63%">
Provides notification of a completed asynchronous I/O operation.

</td>
</tr>
</table> 

