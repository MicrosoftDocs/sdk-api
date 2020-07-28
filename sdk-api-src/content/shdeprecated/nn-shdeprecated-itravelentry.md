---
UID: NN:shdeprecated.ITravelEntry
title: ITravelEntry (shdeprecated.h)
description: Deprecated. Exposes methods to identify, invoke, and update an individual item in the browser's travel history.
helpviewer_keywords: ["ITravelEntry","ITravelEntry interface [Windows Shell]","ITravelEntry interface [Windows Shell]","described","shdeprecated/ITravelEntry","shell.ITravelEntry","zone_ITravelEntry"]
old-location: shell\ITravelEntry.htm
tech.root: shell
ms.assetid: b8a5d532-c1fd-4302-b983-cc9a74270321
ms.date: 12/05/2018
ms.keywords: ITravelEntry, ITravelEntry interface [Windows Shell], ITravelEntry interface [Windows Shell],described, shdeprecated/ITravelEntry, shell.ITravelEntry, zone_ITravelEntry
f1_keywords:
- shdeprecated/ITravelEntry
dev_langs:
- c++
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
- ITravelEntry
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# ITravelEntry interface


## -description


Deprecated. Exposes methods to identify, invoke, and update an individual item in the browser's travel history.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITravelEntry</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITravelEntry</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravelentry-getpidl">GetPidl</a>
</td>
<td align="left" width="63%">
Deprecated. Gets the PIDL associated with the travel entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravelentry-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Deprecated. Invokes the travel entry, navigating to that page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravelentry-update">Update</a>
</td>
<td align="left" width="63%">
Deprecated. Updates the travel entry.

</td>
</tr>
</table> 


## -remarks



Travel entries represented by <b>ITravelEntry</b> are created and maintained internally by the travel log (<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nn-shdeprecated-itravellog">ITravelLog</a>). Calling applications rarely use <b>ITravelEntry</b> directly.

<div class="alert"><b>Note</b>  <b>ITravelEntry</b> may not be supported in versions of Windows later than Windows XP.</div>
<div> </div>


