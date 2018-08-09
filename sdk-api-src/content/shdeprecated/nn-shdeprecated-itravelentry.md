---
UID: NN:shdeprecated.ITravelEntry
title: ITravelEntry
author: windows-sdk-content
description: Deprecated. Exposes methods to identify, invoke, and update an individual item in the browser's travel history.
old-location: shell\ITravelEntry.htm
old-project: shell
ms.assetid: b8a5d532-c1fd-4302-b983-cc9a74270321
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITravelEntry, ITravelEntry interface [Windows Shell], ITravelEntry interface [Windows Shell],described, shdeprecated/ITravelEntry, shell.ITravelEntry, zone_ITravelEntry
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
tech.root: 
req.typenames: BNSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - ITravelEntry
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# ITravelEntry interface


## -description


Deprecated. Exposes methods to identify, invoke, and update an individual item in the browser's travel history.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITravelEntry</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITravelEntry</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITravelEntry</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a3a156f-4d61-4987-b1d8-9e77564d3962">GetPidl</a>
</td>
<td align="left" width="63%">
Deprecated. Gets the PIDL associated with the travel entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21af8d98-f7b6-4204-b855-a4789492a882">Invoke</a>
</td>
<td align="left" width="63%">
Deprecated. Invokes the travel entry, navigating to that page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a>
</td>
<td align="left" width="63%">
Deprecated. Updates the travel entry.

</td>
</tr>
</table> 


## -remarks



Travel entries represented by <b>ITravelEntry</b> are created and maintained internally by the travel log (<a href="https://msdn.microsoft.com/820869aa-ca93-4bb5-831a-3afb52da5389">ITravelLog</a>). Calling applications rarely use <b>ITravelEntry</b> directly.

<div class="alert"><b>Note</b>  <b>ITravelEntry</b> may not be supported in versions of Windows later than Windows XP.</div>
<div> </div>


