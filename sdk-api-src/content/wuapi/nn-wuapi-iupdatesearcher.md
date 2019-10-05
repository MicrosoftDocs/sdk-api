---
UID: NN:wuapi.IUpdateSearcher
title: IUpdateSearcher (wuapi.h)
author: windows-sdk-content
description: Searches for updates on a server.
old-location: wua\iupdatesearcher.htm
tech.root: Wua_Sdk
ms.assetid: f41b1689-d9fe-4697-91e9-a176d3b592c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUpdateSearcher, IUpdateSearcher interface [Windows Update Agent], IUpdateSearcher interface [Windows Update Agent],described, wua.iupdatesearcher, wuapi/IUpdateSearcher
ms.topic: interface
f1_keywords: 
 - "wuapi/IUpdateSearcher"
dev_langs:
 - c++
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
 - IUpdateSearcher
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdateSearcher interface


## -description


Searches for updates on a server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateSearcher</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUpdateSearcher</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-beginsearch">BeginSearch</a>
</td>
<td align="left" width="63%">
Begins execution of an asynchronous search for updates. The search uses the search options that are currently configured.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-endsearch">EndSearch</a>
</td>
<td align="left" width="63%">
Completes an asynchronous search for updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-escapestring">EscapeString</a>
</td>
<td align="left" width="63%">
Converts a string into a string that can be used as a literal value in a search criteria string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-gettotalhistorycount">GetTotalHistoryCount</a>
</td>
<td align="left" width="63%">
Returns the number of update events on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-queryhistory">QueryHistory</a>
</td>
<td align="left" width="63%">
Synchronously queries the computer for the history of update events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-search">Search</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice">CanAutomaticallyUpgradeService</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Boolean value that indicates whether future calls to the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-beginsearch">BeginSearch</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-search">Search</a> methods result in an automatic upgrade to Windows Update Agent (WUA).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid">ClientApplicationID</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates">IncludePotentiallySupersededUpdates</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_online">Online</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_serverselection">ServerSelection</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a <a href="https://docs.microsoft.com/windows/desktop/api/wuapicommon/ne-wuapicommon-serverselection">ServerSelection</a> value that indicates the server to search for updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_serviceid">ServiceID</a>


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



