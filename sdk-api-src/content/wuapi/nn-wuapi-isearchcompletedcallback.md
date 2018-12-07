---
UID: NN:wuapi.ISearchCompletedCallback
title: ISearchCompletedCallback
author: windows-sdk-content
description: Contains a method that handles the notification about the completion of an asynchronous search operation.
old-location: wua\isearchcompletedcallback.htm
tech.root: wua_sdk
ms.assetid: f228808d-7f7e-4107-a4b6-4bac5b48d1b4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISearchCompletedCallback, ISearchCompletedCallback interface [Windows Update Agent], ISearchCompletedCallback interface [Windows Update Agent],described, wua.isearchcompletedcallback, wuapi/ISearchCompletedCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - ISearchCompletedCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISearchCompletedCallback interface


## -description


Contains a method that handles the notification about the completion of an asynchronous search operation. This interface is implemented by programmers who call the <a href="https://msdn.microsoft.com/8af818b1-7dd8-4f48-b447-5b6dfbfce420">IUpdateSearcher.BeginSearch</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchCompletedCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchCompletedCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchCompletedCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d06754a-5750-4986-9f54-98f91dcc705b">Invoke</a>
</td>
<td align="left" width="63%">
Handles the notification of the completion of an asynchronous search initiated by calling <a href="https://msdn.microsoft.com/8af818b1-7dd8-4f48-b447-5b6dfbfce420">IUpdateSearcher.BeginSearch</a>


</td>
</tr>
</table> 

