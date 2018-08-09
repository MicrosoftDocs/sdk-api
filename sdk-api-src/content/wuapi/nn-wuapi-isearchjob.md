---
UID: NN:wuapi.ISearchJob
title: ISearchJob
author: windows-sdk-content
description: Contains properties and methods that are available to a search operation.
old-location: wua\isearchjob.htm
old-project: wua_sdk
ms.assetid: aec4a812-cf5d-4986-a776-29c366bb1771
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchJob, ISearchJob interface [Windows Update Agent], ISearchJob interface [Windows Update Agent],described, wua.isearchjob, wuapi/ISearchJob
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - ISearchJob
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# ISearchJob interface


## -description


Contains properties and methods that are available to a search operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchJob</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ISearchJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISearchJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35f345ac-cf5b-4ba6-9422-5d9da449bcdd">CleanUp</a>
</td>
<td align="left" width="63%">
Waits for an asynchronous operation to complete and then releases all the callbacks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ceedfa28-eef3-4707-8e3a-e59ad45dbea7">RequestAbort</a>
</td>
<td align="left" width="63%">
Makes a request to cancel an asynchronous search.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchJob</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/68d861a3-420d-4a89-ac32-900db6d51036">AsyncState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the caller-specific state object that is passed to the <a href="https://msdn.microsoft.com/8af818b1-7dd8-4f48-b447-5b6dfbfce420">IUpdateSearch.BeginSearch</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/32bb990d-89ce-4aca-8a9f-28cbd991e506">IsCompleted</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the call to the <a href="https://msdn.microsoft.com/8af818b1-7dd8-4f48-b447-5b6dfbfce420">IUpdateSearch.BeginSearch</a> method is completely processed.

</td>
</tr>
</table> 

