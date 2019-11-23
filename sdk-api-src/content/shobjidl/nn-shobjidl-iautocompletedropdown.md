---
UID: NN:shobjidl.IAutoCompleteDropDown
title: IAutoCompleteDropDown (shobjidl.h)

description: Exposes methods that allow clients to reset or query the display state of the autocomplete drop-down list, which contains possible completions to a string entered by the user in an edit control.
old-location: shell\IAutoCompleteDropDown.htm
tech.root: shell
ms.assetid: 1f956d61-6a09-464e-bfe8-0b3bcb9ea181

ms.date: 12/05/2018
ms.keywords: IAutoCompleteDropDown, IAutoCompleteDropDown interface [Windows Shell], IAutoCompleteDropDown interface [Windows Shell],described, _shell_IAutoCompleteDropDown, shell.IAutoCompleteDropDown, shobjidl/IAutoCompleteDropDown
ms.topic: interface
f1_keywords: 
 - "shobjidl/IAutoCompleteDropDown"
dev_langs:
 - c++
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Browseui.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Browseui.dll
api_name:
 - IAutoCompleteDropDown
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAutoCompleteDropDown interface


## -description


Exposes methods that allow clients to reset or query the display state of the autocomplete drop-down list, which contains possible completions to a string entered by the user in an edit control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutoCompleteDropDown</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAutoCompleteDropDown</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAutoCompleteDropDown</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iautocompletedropdown-getdropdownstatus">GetDropDownStatus</a>
</td>
<td align="left" width="63%">
Gets the current display status of the autocomplete drop-down list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iautocompletedropdown-resetenumerator">ResetEnumerator</a>
</td>
<td align="left" width="63%">
Forces the autocomplete object to refresh its list of suggestions when the list is visible.

</td>
</tr>
</table> 

