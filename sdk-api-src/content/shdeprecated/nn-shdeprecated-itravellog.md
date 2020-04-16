---
UID: NN:shdeprecated.ITravelLog
title: ITravelLog (shdeprecated.h)
description: Deprecated. Exposes methods that maintain and manipulate a record of travel in the browser.helpviewer_keywords: ["ITravelLog","ITravelLog interface [Windows Shell]","ITravelLog interface [Windows Shell]","described","shdeprecated/ITravelLog","shell.ITravelLog","zone_ITravelLog"]
old-location: shell\ITravelLog.htm
tech.root: shell
ms.assetid: 820869aa-ca93-4bb5-831a-3afb52da5389
ms.date: 12/05/2018
ms.keywords: ITravelLog, ITravelLog interface [Windows Shell], ITravelLog interface [Windows Shell],described, shdeprecated/ITravelLog, shell.ITravelLog, zone_ITravelLog
f1_keywords:
- shdeprecated/ITravelLog
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
- ITravelLog
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# ITravelLog interface


## -description


<p class="CCE_Message">[<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nn-shdeprecated-itravelentry">ITravelEntry</a> may not be supported in versions of Windows later than Windows XP.]

Deprecated. Exposes methods that maintain and manipulate a record of travel in the browser.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITravelLog</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITravelLog</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-addentry">AddEntry</a>
</td>
<td align="left" width="63%">
Deprecated. Adds a new entry for a pending navigation to the travel log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-clone">Clone</a>
</td>
<td align="left" width="63%">
Deprecated. Duplicates the contents of the current travel log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-countentries">CountEntries</a>
</td>
<td align="left" width="63%">
Deprecated. Generates the number of entries in the travel log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-findtravelentry">FindTravelEntry</a>
</td>
<td align="left" width="63%">
Deprecated. Determines whether a specific travel entry is present in the travel log.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-gettooltiptext">GetToolTipText</a>
</td>
<td align="left" width="63%">
Deprecated. Gets tooltip text for a travel entry, which is used as a Unicode display string in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-gettravelentry">GetTravelEntry</a>
</td>
<td align="left" width="63%">
Deprecated. Gets a travel entry in the travel log relative to the position of the current entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-insertmenuentries">InsertMenuEntries</a>
</td>
<td align="left" width="63%">
Deprecated. Inserts entries into the specified menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-revert">Revert</a>
</td>
<td align="left" width="63%">
Deprecated. Reverts to the current entry, dropping the result of <a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-addentry">ITravelLog::AddEntry</a> in the case of a failed navigation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-travel">Travel</a>
</td>
<td align="left" width="63%">
Deprecated. Navigates to a travel entry in the travel log relative to the position of the current entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-updateentry">UpdateEntry</a>
</td>
<td align="left" width="63%">
Deprecated. Saves the browser state of the current entry in preparation for a pending navigation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-updateexternal">UpdateExternal</a>
</td>
<td align="left" width="63%">
Deprecated. Updates an entry that originated out of the current procedure through <a href="https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)">IHlinkFrame</a>.

</td>
</tr>
</table> 

