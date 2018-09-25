---
UID: NN:shdeprecated.ITravelLog
title: ITravelLog
author: windows-sdk-content
description: Deprecated. Exposes methods that maintain and manipulate a record of travel in the browser.
old-location: shell\ITravelLog.htm
tech.root: shell
ms.assetid: 820869aa-ca93-4bb5-831a-3afb52da5389
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITravelLog, ITravelLog interface [Windows Shell], ITravelLog interface [Windows Shell],described, shdeprecated/ITravelLog, shell.ITravelLog, zone_ITravelLog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - ITravelLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# ITravelLog interface


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/b8a5d532-c1fd-4302-b983-cc9a74270321">ITravelEntry</a> may not be supported in versions of Windows later than Windows XP.]

Deprecated. Exposes methods that maintain and manipulate a record of travel in the browser.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITravelLog</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITravelLog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITravelLog</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f83c1cb1-3cc5-413c-826b-ff4971cd4598">AddEntry</a>
</td>
<td align="left" width="63%">
Deprecated. Adds a new entry for a pending navigation to the travel log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/546581f1-648d-4817-b3d2-aca219b74911">Clone</a>
</td>
<td align="left" width="63%">
Deprecated. Duplicates the contents of the current travel log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/490f7350-6c67-4c79-a100-af266b269472">CountEntries</a>
</td>
<td align="left" width="63%">
Deprecated. Generates the number of entries in the travel log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/128627f3-c010-4b8e-b067-fdc1eed346e4">FindTravelEntry</a>
</td>
<td align="left" width="63%">
Deprecated. Determines whether a specific travel entry is present in the travel log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a085fe2e-9658-448c-b659-4ef08896ec77">GetToolTipText</a>
</td>
<td align="left" width="63%">
Deprecated. Gets tooltip text for a travel entry, which is used as a Unicode display string in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8db8aa9a-91c2-49fb-bbef-c7e19de09efe">GetTravelEntry</a>
</td>
<td align="left" width="63%">
Deprecated. Gets a travel entry in the travel log relative to the position of the current entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e75c524-5fa6-4d76-8fe9-a69ee1b509e8">InsertMenuEntries</a>
</td>
<td align="left" width="63%">
Deprecated. Inserts entries into the specified menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/202ce028-d64c-4733-8006-1bdb1efa8ad3">Revert</a>
</td>
<td align="left" width="63%">
Deprecated. Reverts to the current entry, dropping the result of <a href="https://msdn.microsoft.com/f83c1cb1-3cc5-413c-826b-ff4971cd4598">ITravelLog::AddEntry</a> in the case of a failed navigation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eabe809a-dc02-40fc-9847-88df4cb53e44">Travel</a>
</td>
<td align="left" width="63%">
Deprecated. Navigates to a travel entry in the travel log relative to the position of the current entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63fe398d-c0e8-4350-9b57-fe9f11e24e47">UpdateEntry</a>
</td>
<td align="left" width="63%">
Deprecated. Saves the browser state of the current entry in preparation for a pending navigation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fda446d-8652-455b-9233-aa02f2a85e7f">UpdateExternal</a>
</td>
<td align="left" width="63%">
Deprecated. Updates an entry that originated out of the current procedure through <a href="_inet_IHlinkFrame_Interface_cpp">IHlinkFrame</a>.

</td>
</tr>
</table> 

