---
UID: NN:wuapi.IUpdateSearcher
title: IUpdateSearcher
author: windows-sdk-content
description: Searches for updates on a server.
old-location: wua\iupdatesearcher.htm
old-project: Wua_Sdk
ms.assetid: f41b1689-d9fe-4697-91e9-a176d3b592c7
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IUpdateSearcher, IUpdateSearcher interface [Windows Update Agent], IUpdateSearcher interface [Windows Update Agent],described, wua.iupdatesearcher, wuapi/IUpdateSearcher
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
 - IUpdateSearcher
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateSearcher interface


## -description


Searches for updates on a server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateSearcher</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IUpdateSearcher</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUpdateSearcher</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8af818b1-7dd8-4f48-b447-5b6dfbfce420">BeginSearch</a>
</td>
<td align="left" width="63%">
Begins execution of an asynchronous search for updates. The search uses the search options that are currently configured.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a0532ec-3613-4aa1-96d7-7291b9ca7a94">EndSearch</a>
</td>
<td align="left" width="63%">
Completes an asynchronous search for updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27d510da-3d0c-4a8a-89c9-4abc009489b4">EscapeString</a>
</td>
<td align="left" width="63%">
Converts a string into a string that can be used as a literal value in a search criteria string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/895f60c2-c106-4088-9a4f-7c1d159d8a9b">GetTotalHistoryCount</a>
</td>
<td align="left" width="63%">
Returns the number of update events on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d3027a2-ba97-4dfc-9a15-c106aaf6c2b9">QueryHistory</a>
</td>
<td align="left" width="63%">
Synchronously queries the computer for the history of update events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/mt219145">Search</a>
</td>
<td align="left" width="63%">
Performs a synchronous search for updates. The search uses the search options that are currently configured.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateSearcher</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/115a637d-0b70-4d33-a9c1-43d2faf79067">CanAutomaticallyUpgradeService</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Boolean value that indicates whether future calls to the <a href="https://msdn.microsoft.com/8af818b1-7dd8-4f48-b447-5b6dfbfce420">BeginSearch</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/mt219145">Search</a> methods result in an automatic upgrade to Windows Update Agent (WUA).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5b9ae823-5304-4ec4-937e-684d35bd3aed">ClientApplicationID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Identifies the current client application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e01be972-e5d1-4b37-9ac4-cf9966ed0a4d">IncludePotentiallySupersededUpdates</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Boolean value that indicates whether the search results  include updates that are superseded by other updates in the search results.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Boolean value that indicates  whether the <b>UpdateSearcher</b> goes online to search for updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b514545a-d983-491b-9a28-540bd5c4c128">ServerSelection</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a <a href="https://msdn.microsoft.com/51caac5e-98a6-49e4-a175-6319349a6d68">ServerSelection</a> value that indicates the server to search for updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7c00d26a-9ef0-45ec-81b3-d13f91dd7d8d">ServiceID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a site to search when the site to search is not a Windows Update site.

</td>
</tr>
</table> 


## -remarks



You can create an instance of this interface by using the UpdateSearcher coclass. Use the Microsoft.Update.Searcher program identifier to create the object.



